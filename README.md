# Backend tunnel-iot-gateway setup

- ssh pi@10.129.2.251
- ping google.com
- curl -X POST http://192.168.100.1:8090/login.xml --data-urlencode "mode=191" --data-urlencode "username=rnd" --data-urlencode "password=RnD*123456" --data-urlencode "a=1633529001622" --data-urlencode "producttype=0"
#### CLONE THE REPOSITORY
  - git clone https://github.com/iam-rnd/styleunion-sales-mobile-app-api.git
  - cd tagid-iot-gateway
  - ls
  - sudo docker ps
  - cat docker-compose.yml
  - cd ..
  - mkdir  postgres
  - mkdir redis
  - cd tagid-iot-gateway
  - sudo docker-compose up -d
  - sudo docker ps
  - cat __init__.sql
  - python3 -m venv venv
  - ls
  - source venv/bin/activate
  - pip3 install -r requirenments.txt
  - sudo dpkg -i libpq5_11.19-0+deb10u1_armhf.deb        ____________if error is occured
  - sudo apt-get update && apt-get install libpq5 -y     ____________ if error is occured
  - scp libpq5_11.19-0+deb10u1_armhf.deb pi@192.168.71.15:/home/pi
  - sudo dpkg -i libpq5_11.19-0+deb10u1_armhf.deb
  -  sudo apt-get update && apt-get install libpq5 -y
  - sudo bash run_service.sh
  - [initialization db]
  - sudo journalctl -u tagid-iot-gateway.service -f

    https://github.com/CODER4149/your_readme_files/files/11295465/libpq5_11.19-0%2Bdeb10u1_armhf.zip
#### postgres prompt
  - sudo docker exec -it postgres bash
  - psql -U postgres -d postgres
  - \l
  - \c tagid-iot-gateway
  - \dt
  - \q

