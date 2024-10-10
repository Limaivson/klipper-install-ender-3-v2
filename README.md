# klipper-install-ender-3-v2

### Material necessário:
 - Raspberry pi Zero 2 W ou superior;
 - Cabo usb micro B;
 - Fonte de alimentação para o raspberry;
 - Cartão SD.
### Siga estes passos para instalar e utilizar o klipper na impressora 3d ender 3 v2.
 - Instalar um SO no raspberry pi utilizando o raspberry pi imager;
 - Instalar o kiauh:
 
    O kiauh é um script de instalação para facilitar a instalação do klipper. Para instalar é necessário seguir estes passos:
   - Passo 1:

        Instale o git.
   ```
   sudo apt-get update && sudo apt-get install git -y
   ```
   
   - Passo 2: 

        Clone o diretório do kiauh.
   ```
   cd ~ && git clone https://github.com/dw-0/kiauh.git
   ```

   - Passo 3:

        Inicie o kiah.
   ```
    ./kiauh/kiauh.sh
   ```

 - Use o kiauh para buildar o novo firmware da impressora:
 
    - ### Passo 1:
        
        Selecione a opção 4 como na imagem abaixo:

        ![menu](/doc/MenuKIAUH.png)
    
    - ### Passo 2:
        
        Selecione a opção 1 como na imagem abaixo:

        ![menu](/doc/advanced.png)

    - ### Passo 3:
        
        A tela de configuração do klipper será aberta, faça as configurações conforme a imagem abaixo, após isso pressione a tecla "q" para sair e salvar as configurações:

        ![menu](/doc/klipperConfig.png)
    
    - ### Passo 4:
        
        Após acabar o build do firmware tecle ctrl + c para sair do kiauh, o arquivo "klipper/out/klipper.bin" será gerado, copie este arquivo para o cartão SD e com a impressora desligada insira o cartão SD após inserir ligue a impressora e espere 30 segundos para que o firmware seja carregado.

 - Após o firmware ser carregado, a impressora estará pronta para ser utilizada, para configurar o klipper acesse o arquivo "klipper/config/printer.cfg" e copie a configuração deste arquivo: 
    - Com bltouch: [printerWithBltouch.cfg](printerWithBltouch.cfg).
    - Sem bltouch: [printer.cfg](printer.cfg).