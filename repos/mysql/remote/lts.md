## `mysql:lts`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:6c6706ec58d3ac9e925d5f0435c6a923117f68232551b9c8271a294ea72ee331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de4015d5b1f0fa462e43b48c29f8f66eacdd16d11e07aedf3b13533adadd504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:26:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:26:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:26:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:26:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:26:27 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:26:27 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 16 Jan 2026 23:26:27 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Fri, 16 Jan 2026 23:26:27 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:26:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:26:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:26:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Fri, 16 Jan 2026 23:27:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:27:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:27:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:27:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:27:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:27:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023bf5ce6a4829c6b33eed0642d64a38f47927272c4921804abfda8bab0077ca`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24675d42775811c6a521aae8e2b0b47a989f8f35f2f254fdd43f7828c71d07bd`  
		Last Modified: Fri, 16 Jan 2026 23:28:01 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:28:07 GMT  
		Size: 47.8 MB (47815365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b034b0c553cfc069b162e27ecb7ee469e94daeab571d7f5cd3a83b1498eee6`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada6ad8c9d8c75d4beafab09f3234c75c361caa487b16fcc00ea8c5907ba435f`  
		Last Modified: Fri, 16 Jan 2026 23:28:11 GMT  
		Size: 130.9 MB (130931861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdbfdab06595d747aec81e55886fdb0156d0b08d001428224983ccaeea978cd`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:559414d5a80ae23d630ca19319c21f058973449c33226576fc7ce777c6cb4887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bc7ae4fa3c416b37a5fe586eed0fe24ec1c96a10c3ccc34d9f86157d24ab3`

```dockerfile
```

-	Layers:
	-	`sha256:029be1fc012084294f155b71ce8e88e6926982da803de7249b0fdab37f5291b7`  
		Last Modified: Sat, 17 Jan 2026 01:02:24 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f952b3897aca5d7ca620d3d9679845351641265b1dbc3012ea29253abb57e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228462563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da2a12c183ff681379744e7047ff53800e8dfe4b7217b525b4c92ed1728e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:34 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:34 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Fri, 16 Jan 2026 23:31:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:48 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:54 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:0becb120ac404c9cb5053d5f7ab407549476090ac87b8ca2614f187d759c2d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc389471f6a58f4b1f57e8ec9a1ac08ec71b85b32282bb94c1bdef8f918e0f`

```dockerfile
```

-	Layers:
	-	`sha256:cf05006e49674ec49c6960a63fd16768a1ba783574e4feabbf5cf66257c923e9`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json
