# Restrict-cron-to-run-from-browser-or-postman-
How Restrict cron to run from browser or postman :

if($_SERVER['HTTP_X_FORWARDED_FOR'] == 'IP_ADDRESS_OF_YOUR_SERVER' && $_SERVER['HTTP_USER_AGENT'] == 'Wget/1.18 (linux-gnu)'){
    return true; 
}else{
    echo "Authorization Failed to Run this URL";
    exit;
}
