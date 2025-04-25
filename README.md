Các câu lệnh

docker buildx build -t getting-started .

<!-- Kiểm tra các images -->

docker images


<!-- 3000 đầu là cổng muốn chạy trên máy tính : 3000 sau của docker lắng nghe -->
docker run -dp 3000:3000 getting-started



<!-- Cập nhật ứng dụng băng docker -->

<!-- Thực hiện sửa rồi thực hiện build lại images phải có dấu chấm cuối là đường dẫn tới docker -->


docker build -t getting-started .


docker run -dp 3000:3000 getting-started -> sẽ bị lỗi vì thằng cũ đã dùng port này (có thể chạy trên port khác)


hoặc có thể 


docker ps (xem images)


docker stop container_id (hoặc xóa trên docker_deskstop luôn)

hoặc docker rm -f container_id



----- 

Docker HUB

tùy images thì tên sẽ khác

docker push theanh1301/getting-started


-- Database Docker


docker run --rm alpine touch greeting.txt

docker run --rm alpine stat greeting.txt