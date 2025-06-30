# Sử dụng image có JDK 21
FROM eclipse-temurin:21-jdk-alpine

# Tạo thư mục app
WORKDIR /app

# Copy toàn bộ mã nguồn vào image
COPY . /app

# Cài Maven và build ứng dụng
RUN ./mvnw package -DskipTests

# Expose port (phải trùng với server.port trong application.yml)
EXPOSE 8080

# Lệnh để chạy ứng dụng
CMD ["java", "-jar", "target/demo-1.0-SNAPSHOT.jar"]
