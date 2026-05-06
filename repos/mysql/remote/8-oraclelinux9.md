## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:6e54d72c66fb55fa2bba384cba8c7c0ea9d629fb4d2af613b0eef98d19c6df15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:32d077f0a8de447ece93d7b2fd0bf641654c4da9e2c6336413f7a6ca3ed605cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238255566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a076d4c4d23bbe95ed7197e232b87ed0f0414191f6c64a752b1a9ee24c6b36e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 05 May 2026 23:10:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 05 May 2026 23:10:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 05 May 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:11:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 05 May 2026 23:11:13 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 05 May 2026 23:11:13 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 05 May 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 05 May 2026 23:11:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 05 May 2026 23:11:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 05 May 2026 23:11:43 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 05 May 2026 23:12:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 05 May 2026 23:12:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 May 2026 23:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:12:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 05 May 2026 23:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6405a7c8d60ba5b747797ea10664693becec3b54a5144cba4ed5437ae21b1775`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221f853f73e3a0e8cfc6880e01178ec1493724e27e9c5ca32b34f44d41306c8`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14e3f115d16c730e8c8d8bf7365448aed1f206d35052fcdacba4925bfda96e9`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 6.2 MB (6173027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba345b2c7a56ee98dcc252b69d46cc6f4fa59212cf534fb56c1cd542db6f640`  
		Last Modified: Tue, 05 May 2026 23:12:51 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c4d53bd50351bf445ce03be851e7dc4cb332efba70f07aada43098a914b49b`  
		Last Modified: Tue, 05 May 2026 23:12:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc828cf283e32108d6666c22bd3e2c78a75bb17d51ce328c1e04a7c8453c434e`  
		Last Modified: Tue, 05 May 2026 23:12:55 GMT  
		Size: 51.6 MB (51579199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d744359c8b92558fe864167894c3631c65a2df05d47aa3c01c5fa63828de7a1`  
		Last Modified: Tue, 05 May 2026 23:12:53 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c14a42aea5e27e64384da45dfe87c03229b737374c38ad7708da7b0a241cb`  
		Last Modified: Tue, 05 May 2026 23:12:58 GMT  
		Size: 132.4 MB (132400552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85f525ae670344d1f3e6567144c5954fee1e4252244c92843fed0bb6c686301`  
		Last Modified: Tue, 05 May 2026 23:12:55 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aec15e5470b434bc03b66d642a3bc8c7a51623564e548b1ac8802aa67b9dc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ed676f8f6617ecb587a37493c906518d6cfad146be1b702633799e60921c0`

```dockerfile
```

-	Layers:
	-	`sha256:ddffcbfd1039c8a6bdbb6cec57e92f8d51cc1c0af9c13b808d727afb8f62f6aa`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f404c1c8519a7971d2efaa400dd80d3dde1a0cb6eecef5a673ad75512bcb28`  
		Last Modified: Tue, 05 May 2026 23:12:51 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e83c22293436efb21ddb3f8377e8c518823857217cae821af46e88fd60f27960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233043245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea71701f50ada67965a86368546f5660a31b8e5432635b5eb6b3a450970d552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:10:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 05 May 2026 23:10:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 05 May 2026 23:10:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 05 May 2026 23:10:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:10:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 05 May 2026 23:10:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 05 May 2026 23:10:59 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 05 May 2026 23:10:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 05 May 2026 23:11:31 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 05 May 2026 23:11:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 05 May 2026 23:11:31 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 05 May 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 05 May 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 May 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 05 May 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314aa6027e84211caccfd9a5b90260deab28e31778bcaa918d663de1aaf4f51`  
		Last Modified: Tue, 05 May 2026 23:12:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83c1cfd2b7e63757a6705c3721ecf88983623fb6e10358153af24c4e1fe836a`  
		Last Modified: Tue, 05 May 2026 23:12:42 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1526ac455371d8ef76352e4f2eb4aebb78440939cc515500e9203560e3d9283f`  
		Last Modified: Tue, 05 May 2026 23:12:42 GMT  
		Size: 5.8 MB (5790727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949fdcdadbfc49aea424e9853e241ce8c0a9f3d3efd79713c2c1803088b7c5d`  
		Last Modified: Tue, 05 May 2026 23:12:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eadfe64ca3e566a76fefb7c4a9f12e9319d88fff6f62095e7128878743eb0fa`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad3599a02614ba115673a2bfee55456cab16b13722a9aeceac6567dfcd5ab7b`  
		Last Modified: Tue, 05 May 2026 23:12:44 GMT  
		Size: 49.8 MB (49827180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845320a47546f5799bf9983438b8383da18b36b6df1f6ebe1155698cb22cb3ef`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb430fd451ed046f0296763fc8bf04e8c7351689d1433e2dd1e59bdd272e489`  
		Last Modified: Tue, 05 May 2026 23:12:46 GMT  
		Size: 130.8 MB (130779521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2c9176de2742ca296fe885e506bf46b0e2822b0beff90d985d900398cfce1`  
		Last Modified: Tue, 05 May 2026 23:12:44 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:580494bb8c0d9a379d609cabc1a07d9e93716204d0696df05df369b768109845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b798cb824e182880838778ed4d33d1de896168a880546b64d8408a1c884f31f`

```dockerfile
```

-	Layers:
	-	`sha256:f0394b70a80899a0beecc5046514079e2c637ed72d87f680b18b734e60d35820`  
		Last Modified: Tue, 05 May 2026 23:12:42 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d820fbd3364895c27a44e60bf2c82933f81eaff8c9dec35bb7f778697a77c4`  
		Last Modified: Tue, 05 May 2026 23:12:41 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json
