NAMA : FACHRI ABYASA TARID
NIM : J0404241136
KELAS : TRK B2

# command
# nginx
ipbca@abyserver:~$ docker pull nginx

ipbca@abyserver:~$ docker run -d --name web-server -p 8080:80 nginx

# mysql
ipbca@abyserver:~$ docker pull mysql

ipbca@abyserver:~$ docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=root123 -p 3306:3306 mysql

ipbca@abyserver:~$ docker logs mysql-db

# bind9
ipbca@abyserver:~$ docker pull ubuntu/bind9:latest
ipbca@abyserver:~$ docker run -d --name bind9-container -e TZ=UTC -p 30053:53 -p 30053:53/udp ubuntu/bind9:latest
ipbca@abyserver:~$ docker logs bind9-container

# fungsi - fungsi command
docker pull [image]
Menginstall dari docker registry ke local

docker run [container]
Untuk menjalankan container baru


docker logs [image]
Melihat output container

-d 
Container berjlan di background

--name [container]
Memberi nama container

-p 8080:80 [port] 
berfungsi untuk menghubungkan port 80 ke container port 8080

-e MYSQL_ROOT_PASSWORD=root123
Menetapkan password untuk user root MySQL di dalam container.

-e TZ=UTC
Menentukan timezone di dalam container, dalam kasus ini diset ke UTC.

-p 30053:53
Port TCP mapping: Mengarahkan port 53 TCP (DNS) di dalam container ke port 30053 TCP di host.

-p 30053:53/udp
Port UDP mapping: Mengarahkan port 53 UDP (DNS) di container ke port 30053 UDP di host.

# penjelasan layanan
# nginx
ginx adalah perangkat lunak web server dan reverse proxy yang dirancang untuk menangani ribuan koneksi secara simultan dengan penggunaan memori yang rendah.
# mysql
MySQL adalah sistem manajemen basis data relasional open source yang menyimpan informasi dalam tabel dan memungkinkan pengelolaan data melalui bahasa SQL

# bind9
BIND9 (Berkeley Internet Name Domain versi 9) berfungsi sebagai server DNS utama dengan kemampuan menerjemahkan nama domain menjadi alamat IP dan sebaliknya

# link image resmi
nginx
https://hub.docker.com/r/nginx
mysql
https://hub.docker.com/r/mysql
bind9
https://hub.docker.com/r/ubuntu/bind9
