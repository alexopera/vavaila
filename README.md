@AleoFaucet send 10 credits to aleo1y9s2yr50paljp0rd8wtqzy6ue9cshyyukwfslx2vhpj588vnguzqnndumr

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

snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "" --path "./${APPNAME}/build/" --broadcast "" --fee 600000 --record "${RECORD}"

    
