## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:0f775a92980b41c87c58f934a204de80431dd4d854057160ec1cb936663eabe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:60832e27fa98532ef7b75e634b065dd3809fcfbbe0dc591d6adf30a386d4dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232889705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e963ded2487039d333ce0462f0b5469c1ce235cb595a1071653ec224884993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f5383682500ad1bc21ff033196db4481516e58b90b30bf54f33321663fe052`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec3ee0f0f087338cdaffbb8c439c712690c5957df73c620a1df5bb383153c27`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d64c2aa182d2039eff88a90e02b11d0929be010535f6561ab4f21c37113f2f6`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 6.9 MB (6893168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779c43f7638554d6e405b099dbd3deb634e50bb06b674ac5a767f686914b242e`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d08e04e916ff21e89523b66e600686ddfef2f3716b2cc9209897be42c7c60db`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c324f526407a21e9975b701eaf417f5078572c345ce10912ca017e1fe378f5f0`  
		Last Modified: Thu, 13 Mar 2025 17:53:22 GMT  
		Size: 47.6 MB (47585886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78747d9f656f8159420d6a817c650b724d12e7a27cf158bed2ee25a8ea0da33`  
		Last Modified: Thu, 13 Mar 2025 17:53:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd85f24b56a2fa0c6c4497f8cac542ecc94e01a22216b159e0c5e24dfe05fee`  
		Last Modified: Thu, 13 Mar 2025 17:53:24 GMT  
		Size: 128.3 MB (128326738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a2795e87567187c8f5d2346f46600edb86a7c7960ca2dcbfce97262d9d7c00`  
		Last Modified: Thu, 13 Mar 2025 17:53:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6bee652a54a90d9de7169e7c8d8df56805155e06f687625760cedd7ca326a294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097ce9f0e436e3c004ec062b1be577711a9242bc36868aeddcc3611cf679a581`

```dockerfile
```

-	Layers:
	-	`sha256:3eb6c8556c142c66780774045bc0c89b880bba25bb2f80d9286d2fe63beb6b91`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a0672ba01ff31b774e2e36c2f84d8e64db50598d0ac9a6b069a87dee32bd81`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2eb1304aed9a34e5889d743bbb82d03a301239faff5556edb63fac11e4d5eb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2522ece9d722de65778e3a020f5e11271d3a58d91565c49547f9523ecb23d2eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2303f4a62c55de3c5666d328252495ec3eb67947cc5d75d3d46ae3d8353badbc`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d763704225c6d5b23348b25756defb363cf11fc94265a689a18a1509964c25f5`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d056028b9c184a140e5804abd9168fd02c6fc091e4859ef66373837675ed4ec4`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 6.5 MB (6486308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b1500def330ca832518ff9cda277c50a449359f5ffd9e3093f8b9e67671615`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b1a00c4fbb742b318594c4fb7b4e87694f0453f39251f0fc1f1d456f13609c`  
		Last Modified: Thu, 13 Mar 2025 19:14:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785027c0cc36203fb28a3d82066d4eaa1612ca30cfd9b07e381296396fb1db24`  
		Last Modified: Thu, 13 Mar 2025 19:14:38 GMT  
		Size: 46.5 MB (46464142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537c886a8c05fd1825353231362f5a33566af7d4e2eb8fea8c7796d666baaa6`  
		Last Modified: Thu, 13 Mar 2025 19:14:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002294f6f57705ec3502892d9335fe8089d44a3d399c5ecd96a0197546f6734f`  
		Last Modified: Thu, 13 Mar 2025 19:14:40 GMT  
		Size: 126.8 MB (126792326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e2abd5b2e9a9e85d6bd3e4434123450b9536b957d7e93da4744722110542f`  
		Last Modified: Thu, 13 Mar 2025 19:14:37 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4b34e99206538b11c3f655fdd715a426bccf280bd00b4f4b7506a1d14e6b7afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e65148744d1d411d1e7314cd122f7d465916ea74e38913ddf34d39ec92d28d3`

```dockerfile
```

-	Layers:
	-	`sha256:5670842226fb6347aeb06762dc3bee099cd6fe952d837744b5045bde5f1f2fb7`  
		Last Modified: Thu, 13 Mar 2025 19:14:37 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d97715008e5187cfc23aa693c272fac1d708f26f78813ec054d761b9efe5f8`  
		Last Modified: Thu, 13 Mar 2025 19:14:36 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json
