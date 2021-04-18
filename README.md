<h3># Payment-Gateway</h3><h3 style="color:green">Designed by Mohammad Saquib Khan</h3>
<h4># How to install the sample kit on a web server:<br>
 1. Copy PaytmKit folder in document root of your server (like /var/www/html)<br>
 2. Open config_paytm.php file from the PaytmKit/lib folder and update the below constant values<br>
    - PAYTM_MERCHANT_KEY – Provided by Paytm<br>
    - PAYTM_MERCHANT_MID - Provided by Paytm<br>
    - PAYTM_MERCHANT_WEBSITE - Provided by Paytm<br>
 3. PaytmKit folder is having following files:<br>
    - TxnTest.php – Testing transaction through Paytm gateway.<br>
    - pgRedirect.php – This file has the logic of checksum generation and passing all required parameters to Paytm PG.<br> 
    - pgResponse.php – This file has the logic for processing PG response after the transaction        processing.<br>
    - TxnStatus.php – Testing Status Query API<br></h4>

<h3># For Offline(Wallet Api) Checksum Utility below are the methods:</h3><br>
<h4>  1. getChecksumFromString : For generating the checksum<br>
  2. verifychecksum_eFromStr : For verifing the checksum<br></h4>
  
<h3># To generate refund checksum in PHP :</h3>
  <h4>1. Create an array with key value pair of following paytm parameters<br> 
     (MID, ORDERID, TXNTYPE, REFUNDAMOUNT, TXNID, REFID)<br>
  2. To generate checksum, call the following method. This function returns the checksum as a string.<br>
     getRefundChecksumFromArray($arrayList, $key, $sort=1)<br>
</h4>
