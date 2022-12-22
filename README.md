# docker_example_spring
docker_test

IntelliJ 
 1. Maven 탭에서 LifeCycle/test - Click Toggle 'Skip Tests' Mode 
 2. Execute Maven Goal - Click package
 3. Click LifeCycle/pacakage
 4. Project / target 폴더에서 jar파일 확인 

DeskTop
1. 해당 프로젝트 폴더에서 dockerfile(확장자 없이, 소문자로만 가능)파일 생성
2. 메모장 연결 후  FROM adoptopenjdk/openjdk11
                  ARG JAR_FILE=target/*.jar
                  COPY ${JAR_FILE} app.jar
                  ENTRYPOINT ["java", "-jar", "/app.jar"]
                  작성

cmd
1. 해당 폴더 디렉토리에서 cmd 실행후 docker build -t 각자id/springbootdocker ./ 입력
2. docker run -p 60080:8080 -d 각자id/springbootdocker
3. localhost:60080 확인

Dockerhub로 이미지 PUSH
1.도커 로그인 $ docker login
2. 도커에 푸시 $ docker push id/springbootdocker
