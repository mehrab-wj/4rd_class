### 4rd class | a simple class for submit request to 4rd.ir 
download and include this class to your project and submit request to 4rd.ir API's easiestly !

## create order:
````
<?php
include_once('4rd.php');
$_4rd = new _4rd();

$order = $_4rd->request(['action'=>'new_order','service'=>$service_id,'count'=>$count,'link'=>$link]);
    if ($order->result == "ok") {
      echo 'order submited successfully!';
    }
    else {
      echo $order->message;
    }
  
?>
````
## check account status: 
````
<?php
include_once('4rd.php');
$_4rd = new _4rd();

$check_account = $_4rd->request(['action'=>'account_check']);
  if ($check_account->result == "ok") {
    echo 'token is correct ! \n
    your account balance: '.$check_account->cash;
  }
  else {
    echo 'incorrect token ! \n
    please change your token from 4rd.php';
  }
  
?>
````
