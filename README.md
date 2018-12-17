# login_google_ionic

https://www.youtube.com/watch?v=NFUN3MIb0GE
https://ionicframework.com/docs/native/google-plus/
(https://www.npmjs.com/package/cordova-plugin-googleplus)  WEB_APPLICATION_CLIENT_ID

1) console.developers.google.com > credentials > tela de concentimento OAuTh:
 1.1 configurar concentimento 
 1.2 criar o cliente Oauth

2)Executar comando na pasta do projeto> keytool -exportcert -alias androiddebugkey -keystore ~/.android/debug.keystore -list -v
 2.1 copiar o SHA1..
 2.2 Em config.xm l> copiar o Widget id..
 
 3) executar comando na pasta do projeto
  3.1 ionic cordova plugin add cordova-plugin-googleplus --variable REVERSED_CLIENT_ID=myreversedclientid --variable WEB_APPLICATION_CLIENT_ID=
  
  4) habilitar a api Google + plus.
  5) dentro da APi habilitada criar as credencial
  6) npm install --save @ionic-native/google-plus
  
  import { GooglePlus } from '@ionic-native/google-plus';

constructor(private googlePlus: GooglePlus) { }

...

this.googlePlus.login({})
  .then(res => console.log(res))
  .catch(err => console.error(err));
