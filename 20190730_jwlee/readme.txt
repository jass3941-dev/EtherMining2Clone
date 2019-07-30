사용설명서 

- 제한사항( PreRequisite )

  1. 현재 버전은 64bit 버전의 리눅스 및 윈도우에만 적용된다.( 32Bit 버전은 지원하지 않는다. )
  2. Windows 버전은 Window 10 Home, Professional, Enterprise 버전에서 VM으로 테스트되었다.
  3. Linux 버전은 Ubuntu 18.04 버전에서 테스트되었으나 CentOS나 다른 배포판에서도 동일하게 동작하게끔 빌드되었다.
  4. PGP 개인서명을 위한 ShaHash 256으로 Sign되었다.( 옵션으로 패키지가 제대로 다운받았느지 체크할 수 있다.)
  
- Windows 마이너 설치 
  1. ethminer.zip 을 https://github.com/jasss3941/EtherMining2Clone/blob/master/20190730_jwlee/Window/ethminer.zip 에서 다운받는다
  2. 윈도우의 임의 디렉터리를 만들고 ( 예 C:\Miners ) 다운받은 ethminer.zip 파일을 복사한다.
  3. 임의의 디렉터리에 파일을 압축해제하면 아래의 파일이 생긴다.
     - 현재디렉터리\bin\kernels\ethash_baffin_lws64.bin,~ ,ethash_tonga_lws256.bin( 총 16개의 바이너리 cl 커널파일 )
     - 현재디렉터리\bin\ethminer.exe 
  4. https://github.com/jasss3941/EtherMining2Clone/tree/master/20190730_jwlee/Window 에서 startup.bat 파일을 다운받는다.
  5. startup.bat 파일을 현재디렉터리\bin 밑에 복사하고 내용을 편집한다. 편집할 내용은 아래와 같다.
     - ethminer.exe -G -P stratum2+tcp://jasss3941%%2ewindowtest:x@asia.ethash-hub.miningpoolhub.com:20535  --cl-local-work 256 --opencl-platform 1
     - 위에서 편집할 내용은 jasss3941( 마플허아이디)와 windowtest( 마이너 이름)을 본인에 맞게 수정한 후 명령프롬프트를 연 후 실행시키면 된다.
     - 주의사항은 마플허아이디와 마이너이름사이의 %%2e 은 두 마플허아이디와 마이너이름을 정규표현식으로 구분하기 위해서 
       필요한 특수문자인데 윈도우와 리눅스가 다르므로 각별히 주의하여야 한다.
       
- Linux 마이너 설치 
  1. ethminer.tar.gz 을 https://github.com/jasss3941/EtherMining2Clone/blob/master/20190730_jwlee/Linux/ethminer.tar.gz 에서 다운받는다
  2. 리눅스의 임의 디렉터리를 만들고 ( 예 mkdir Miners ) 다운받은 ethminer.tar.gz 파일을 복사한다.
  3. 임의의 디렉터리에 파일을 압축해제( 예 tar xvf ethminer.tar.gz )하면 아래의 파일이 생긴다.
     - ./Binary/kernels/ethash_baffin_lws64.bin,~ ,ethash_tonga_lws256.bin( 총 16개의 바이너리 cl 커널파일 )
     - ./Binary/ethminer
  4. https://github.com/jasss3941/EtherMining2Clone/blob/master/20190730_jwlee/Linux/ 에서 startup.sh 파일을 다운받는다.
  5. startup.sh 파일을 현재디렉터리\Binary 밑에 복사하고 내용을 편집한다. 편집할 내용은 아래와 같다.
     - #!/bin/sh
       ./ethminer -v 3 -G -P stratum2+tcp://jasss3941%2eminertest:x@asia1.ethereum.miningpoolhub.com:20535 --cl-local-work 256
     - 위에서 편집할 내용은 jasss3941( 마플허아이디)와 windowtest( 마이너 이름)을 본인에 맞게 수정한 후 명령프롬프트를 연 후 실행시키면 된다.
     - 주의사항은 마플허아이디와 마이너이름사이의 %2e 은 두 마플허아이디와 마이너이름을 정규표현식으로 구분하기 위해서 
       필요한 특수문자인데 윈도우와 리눅스가 다르므로 각별히 주의하여야 한다.
  6. startup.sh 파일에게 실행권한을 준다.( 예 chmod +x startup.sh )
  7. ./startup.sh 으로 현재디렉터리에 있는 startup.sh 파일을 실행한다.
  
문의사항은 아래의 메일을 이용해 주십시오. 
Tech support : jass3941@gmail.com 
이상입니다.
  
  
       
       
     
     

     
     
     
     
     


