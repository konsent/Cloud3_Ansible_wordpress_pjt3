# Ansible 기반 Wordpress 배포 및 DB 인프라 구축 PJT  
    
      
      
  ## 프로젝트 개요 및 목적

   본 프로젝트는 **Playdata Cloud 부트캠프 3기** 교육 커리큘럼 중 Ansible/Vagrant 오픈 소스 자동화 도구에 대한 실습을 그 목적으로 한다.  
   리눅스 OS 가상머신 상에서 WEB 서버와 DB 서버를 구축하고, 구축한 서버 위에 Wordpress 홈페이지를 설치 후 배포한다.



  ## 주요 구현 목표  

  1. Vagrant를 통한 인스턴스 구성 자동화(Master 노드, WEB 및 DB 서버 각 1개 구성)
  2. Ansible Playbook으로 Wordpress 배포에 필요한 패키지 모듈 설치 및 구성



  ## 개발 환경 및 도구  

  - Ubuntu OS(20.04LTS) : UNIX 기반의 OS, WEB/DATABASE 서버의 기본 운영체제 
  
  - PHP(7.4) : HTML 기반의 스크립트 프로그래밍 언어 
  
  - MySQL(5.7) : 오픈소스 방식의 DBMS 프로그램 
  
  - Apache(2.4.41) : http 기반 Web 서버용 소프트웨어 
  
  - Ansible(2.12.4) : 오픈 소스기반 자동화 도구 
  
  - Wordpress(5.9.3) : 홈페이지 생성 및 배포



  ## 주의사항  

  ❌ MySQL 5.7버전이 자동으로 설치되지 않아 DB 서버에 수동으로 MySQL5.7을 설치하였다.  
  Playbook을 그대로 실행할 경우 DB 쪽에서 no_log 관련 에러가 발생하는 것을 확인함  
  
  추후 수정 예정
  
  

  

  
  
  
  


