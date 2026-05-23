# bt4_tudongdangbaiwordpress
# họ và tên : Nguyễn Trung Kiên 
# Lớp K58KMT
# Mssv: K225480106032

# bài tập tự động đăng bài wordpress

# bài làm 

# cấu hình file docker-composegithub
<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/f3c2714a-1c7c-4f44-a78b-113e654faa8e" />
      PMA_ARBITRARY: 1
    depends_on:
      - mariadb

  wordpress:
    image: wordpress:latest
    restart: unless-stopped
    environment:
      WORDPRESS_DB_HOST: mariadb
      WORDPRESS_DB_NAME: wordpress_db
      WORDPRESS_DB_USER: wp_user
      WORDPRESS_DB_PASSWORD: wp_pass123
    volumes:
      - wordpress_data:/var/www/html
    depends_on:
      - mariadb

  cloudflared:
    image: cloudflare/cloudflared:latest
    restart: unless-stopped
    command: tunnel --no-autoupdate run --token eyJhIjoiNmIxNDgzYTUyNzFjMTUxNmIwZmEwOTdmYjdlODllOTMiLCJ0IjoiZTY0YjI4ZTMtYWJiZC00MjNjLWJiODAtMTg3YzY3MTEwNTc>

  n8n:
    image: n8nio/n8n:latest
    restart: unless-stopped
    environment:
      - WEBHOOK_URL=https://k58-n8n.nguyenkien2511.io.vn/
      - N8N_HOST=k58-n8n.nguyenkien2511.io.vn
      - N8N_PROTOCOL=https
    volumes:
      - n8n_data:/home/node/.n8n

volumes:
  mariadb_data:
  wordpress_data:
  n8n_data:

  # running n8n 
  <img width="1901" height="166" alt="image" src="https://github.com/user-attachments/assets/210fa637-ce22-47f0-9b63-92492ce9e97d" />

[+] Running 1/1
 ✔ Container myproject-n8n-1  Running   

 # kiểm tra toàn bộ docker có chạy k 
 
 <img width="1906" height="208" alt="image" src="https://github.com/user-attachments/assets/990fb332-4492-473b-9b04-9feca17043a8" />

 dev-kien@nguyen-kien:~/myproject$ docker compose up -d
WARN[0000] /home/dev-kien/myproject/docker-compose.yml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion
[+] Running 5/5
 ✔ Container myproject-cloudflared-1  Running                                                                                                          0.0s
 ✔ Container myproject-n8n-1          Running                                                                                                          0.0s
 ✔ Container myproject-mariadb-1      Running                                                                                                          0.0s
 ✔ Container myproject-phpmyadmin-1   Running                                                                                                          0.0s
 ✔ Container myproject-wordpress-1    Running                                                                                                          0.0s

# vào trang php admin 

<img width="1865" height="976" alt="image" src="https://github.com/user-attachments/assets/c59d3b61-e7da-48d8-8019-76dadf827ba4" />

https://k58-pma.nguyenkien2511.io.vn/index.php?route=/

# trang workflow
https://k58-n8n.nguyenkien2511.io.vn/

<img width="1907" height="982" alt="image" src="https://github.com/user-attachments/assets/80ee34ef-3085-463b-bbc1-3007ec203c54" />

# trang wordpress
https://k58-wp.nguyenkien2511.io.vn/

<img width="1865" height="965" alt="image" src="https://github.com/user-attachments/assets/4fc84227-ba2d-4d99-b5da-b31583c3f3c9" />

# lấy key telegram 

<img width="1861" height="881" alt="image" src="https://github.com/user-attachments/assets/063862a6-d606-4cc9-8620-00b6d6bdcf7c" />

# cấu hình workflow

<img width="1166" height="485" alt="image" src="https://github.com/user-attachments/assets/a2983c86-01f8-4d46-bdd1-087768be74fa" />

cấu hình telegram 
<img width="1164" height="738" alt="image" src="https://github.com/user-attachments/assets/70ae6bc6-ec9a-4f15-ba20-b55a2aab6da8" />

cấu hình api AI

vì tài khoản google không cho miễn phí lên em chuyển qua http: openAI
<img width="1819" height="814" alt="image" src="https://github.com/user-attachments/assets/e0b3c5fa-3d4f-466c-87c0-0c099c0a1b0b" />

code javascript

<img width="1806" height="798" alt="image" src="https://github.com/user-attachments/assets/e14a154c-74c6-472e-b515-03ad96b8002a" />

cấu hình post 
<img width="1815" height="827" alt="image" src="https://github.com/user-attachments/assets/e74d1335-10e3-425d-9734-4554aa9ce998" />

# Kết quả 

<img width="1919" height="881" alt="image" src="https://github.com/user-attachments/assets/785dd647-151a-4219-a83e-635f092369ac" />


<img width="1164" height="465" alt="image" src="https://github.com/user-attachments/assets/6523e939-d4bc-4f38-9c0b-c8b749903334" />


<img width="1919" height="885" alt="image" src="https://github.com/user-attachments/assets/fc6f53ac-51b0-448d-b325-fcbf70905fe6" />



