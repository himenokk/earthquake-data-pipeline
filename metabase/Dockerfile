# Замените старый openjdk:19-buster на этот:
FROM eclipse-temurin:17-jre-focal

ENV MB_PLUGINS_DIR=/home/plugins/

ADD https://downloads.metabase.com/v0.52.13/metabase.jar /home/metabase.jar
ADD https://github.com/MotherDuck-Open-Source/metabase_duckdb_driver/releases/download/0.2.12-b/duckdb.metabase-driver.jar /home/plugins/

RUN chmod 744 /home/plugins/duckdb.metabase-driver.jar

# Убедитесь, что путь к jar указан верно (я добавил /home/metabase.jar выше)
CMD ["java", "-jar", "/home/metabase.jar"]