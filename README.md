# docker_example_spring
docker_test

IntelliJ      -> 1. Maven 탭에서 LifeCycle/test - Click Toggle 'Skip Tests' Mode 
                 2. Execute Maven Goal - Click package
                 3. Click LifeCycle/pacakage
                 4. Project / target 폴더에서 jar파일 확인 
DeskTop      -> 1. 해당 프로젝트 폴더에서 dockerFile(확장자 없이)파일 생성
                2. 메모장 연결 후  FROM adoptopenjdk/openjdk11
                                  ARG JAR_FILE=target/*.jar
                                  COPY ${JAR_FILE} app.jar
                                  ENTRYPOINT ["java", "-jar", "/app.jar"]
                                  작성
