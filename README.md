@AleoFaucet send 10 credits to aleo1y9s2yr50paljp0rd8wtqzy6ue9cshyyukwfslx2vhpj588vnguzqnndumr

Ø¨Ø¹Ø¯ Ø§Ø² Ø¯Ø±ÛŒØ§ÙØª ÙØ§Ø³Øª Ø¨Ù‡ Ù„ÛŒÙ†Ú© Ø²ÛŒØ± Ø¨Ø±ÛŒØ¯ Ùˆ Ø§ÙØ²ÙˆÙ†Ù‡ Ø±Ø§ Ø¨Ù‡ Ù…Ø±ÙˆØ±Ú¯Ø± Ú©Ø±ÙˆÙ… Ø§Ø¶Ø§ÙÙ‡ Ú©Ù†ÛŒØ¯

https://chrome.google.com/webstore/detail/json-beautifier-editor/lpopeocbeepakdnipejhlpcmifheolpl
------------------------------------------------------------------

cd $HOME

mkdir demo_deploy_Leo_app && cd demo_deploy_Leo_app

WALLETADDRESS=""

APPNAME=helloworld_"${WALLETADDRESS:4:6}"

leo new "${APPNAME}"

PATHTOAPP=$(realpath -q $APPNAME)

cd $PATHTOAPP && cd ..

PRIVATEKEY=""

RECORD=""

snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://vm.aleo.org/api" --path "./${APPNAME}/build/" --broadcast "https://vm.aleo.org/api/testnet3/transaction/broadcast" --fee 600000 --record "${RECORD}"

    
