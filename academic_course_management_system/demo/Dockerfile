FROM eclipse-temurin:21-jdk-alpine

WORKDIR /app

COPY . /app

# Cấp quyền thực thi cho mvnw
RUN chmod +x mvnw

# Build ứng dụng
RUN ./mvnw package -DskipTests

# Mở cổng (phải trùng với application.yml)
EXPOSE 8080

# Chạy ứng dụng
CMD ["java", "-jar", "target/demo-1.0-SNAPSHOT.jar"]

