<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux9`](#mysql80-oraclelinux9)
-	[`mysql:8.0.44`](#mysql8044)
-	[`mysql:8.0.44-bookworm`](#mysql8044-bookworm)
-	[`mysql:8.0.44-debian`](#mysql8044-debian)
-	[`mysql:8.0.44-oracle`](#mysql8044-oracle)
-	[`mysql:8.0.44-oraclelinux9`](#mysql8044-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.7`](#mysql847)
-	[`mysql:8.4.7-oracle`](#mysql847-oracle)
-	[`mysql:8.4.7-oraclelinux9`](#mysql847-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.5`](#mysql95)
-	[`mysql:9.5-oracle`](#mysql95-oracle)
-	[`mysql:9.5-oraclelinux9`](#mysql95-oraclelinux9)
-	[`mysql:9.5.0`](#mysql950)
-	[`mysql:9.5.0-oracle`](#mysql950-oracle)
-	[`mysql:9.5.0-oraclelinux9`](#mysql950-oraclelinux9)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux9`](#mysqlinnovation-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8-oracle` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8-oraclelinux9` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:707f5c087531fde2fe4cd0fa3a125c7467e99b7f6282a3e6ed338604aedb8c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:40925488baf8d5eac689f01e2659e6cf40b4b3bb3c244bba0ba21bd482fdd4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183452646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5aee5818e82c7cf5ff947329e5d962dd39fe020a4ef1e7442b52503918ab16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:26:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 13 Jan 2026 02:26:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:26:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 13 Jan 2026 02:26:49 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jan 2026 02:26:59 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:26:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 13 Jan 2026 02:26:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22e1a2160f42b051b03385b84706675799af27ef1d739855ea53e86c1db3754`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9018174d359de6a5328223860c685beff628396b4c0751bddd67bb6f436fba`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc91177be4b5ddabf028b6195345d9f121dd74538248e72a22d10a6bd5a4337`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.2 MB (1248687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba707135653628509d4c84f1cbe8c4a2cdd97b36d775765d7fc9f2ca48424385`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:22 GMT  
		Size: 15.3 MB (15295770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe1cdeaf5edd760187d6513d256abb23908c164f4a38247388365eea86f5ef`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9fa428fed3bfa308b0a3205123630fdecf4189ddab8c0c3603184bbf94f36b`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fcdfeee6d72380d9c3d4a00158cc023cf4e8540b36d9c4024d2fd4964525d`  
		Last Modified: Tue, 13 Jan 2026 02:27:25 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:23 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:fb4276d47d3a8247eb6723e1cbdd8e5efe29cce9d80ffbb8c7b008535c4d5771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d4fa1a08a98e8b03328728bb4292e3ff94f991594a62e81e53de38cd3d68a`

```dockerfile
```

-	Layers:
	-	`sha256:e8aa42f4ffccc5f8c5c19f5e5058c2ba4dbe2927dd1ecd3022c6c40cea93c05d`  
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851452c4742f43d72b47517aa649b8dabe50ed847fc6bb02d0dda1f097697c17`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:707f5c087531fde2fe4cd0fa3a125c7467e99b7f6282a3e6ed338604aedb8c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:40925488baf8d5eac689f01e2659e6cf40b4b3bb3c244bba0ba21bd482fdd4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183452646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5aee5818e82c7cf5ff947329e5d962dd39fe020a4ef1e7442b52503918ab16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:26:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 13 Jan 2026 02:26:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:26:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 13 Jan 2026 02:26:49 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jan 2026 02:26:59 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:26:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 13 Jan 2026 02:26:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22e1a2160f42b051b03385b84706675799af27ef1d739855ea53e86c1db3754`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9018174d359de6a5328223860c685beff628396b4c0751bddd67bb6f436fba`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc91177be4b5ddabf028b6195345d9f121dd74538248e72a22d10a6bd5a4337`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.2 MB (1248687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba707135653628509d4c84f1cbe8c4a2cdd97b36d775765d7fc9f2ca48424385`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:22 GMT  
		Size: 15.3 MB (15295770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe1cdeaf5edd760187d6513d256abb23908c164f4a38247388365eea86f5ef`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9fa428fed3bfa308b0a3205123630fdecf4189ddab8c0c3603184bbf94f36b`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fcdfeee6d72380d9c3d4a00158cc023cf4e8540b36d9c4024d2fd4964525d`  
		Last Modified: Tue, 13 Jan 2026 02:27:25 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:23 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:fb4276d47d3a8247eb6723e1cbdd8e5efe29cce9d80ffbb8c7b008535c4d5771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d4fa1a08a98e8b03328728bb4292e3ff94f991594a62e81e53de38cd3d68a`

```dockerfile
```

-	Layers:
	-	`sha256:e8aa42f4ffccc5f8c5c19f5e5058c2ba4dbe2927dd1ecd3022c6c40cea93c05d`  
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851452c4742f43d72b47517aa649b8dabe50ed847fc6bb02d0dda1f097697c17`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:707f5c087531fde2fe4cd0fa3a125c7467e99b7f6282a3e6ed338604aedb8c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:40925488baf8d5eac689f01e2659e6cf40b4b3bb3c244bba0ba21bd482fdd4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183452646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5aee5818e82c7cf5ff947329e5d962dd39fe020a4ef1e7442b52503918ab16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:26:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 13 Jan 2026 02:26:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:26:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 13 Jan 2026 02:26:49 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jan 2026 02:26:59 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:26:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 13 Jan 2026 02:26:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22e1a2160f42b051b03385b84706675799af27ef1d739855ea53e86c1db3754`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9018174d359de6a5328223860c685beff628396b4c0751bddd67bb6f436fba`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc91177be4b5ddabf028b6195345d9f121dd74538248e72a22d10a6bd5a4337`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.2 MB (1248687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba707135653628509d4c84f1cbe8c4a2cdd97b36d775765d7fc9f2ca48424385`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:22 GMT  
		Size: 15.3 MB (15295770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe1cdeaf5edd760187d6513d256abb23908c164f4a38247388365eea86f5ef`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9fa428fed3bfa308b0a3205123630fdecf4189ddab8c0c3603184bbf94f36b`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fcdfeee6d72380d9c3d4a00158cc023cf4e8540b36d9c4024d2fd4964525d`  
		Last Modified: Tue, 13 Jan 2026 02:27:25 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:23 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:fb4276d47d3a8247eb6723e1cbdd8e5efe29cce9d80ffbb8c7b008535c4d5771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d4fa1a08a98e8b03328728bb4292e3ff94f991594a62e81e53de38cd3d68a`

```dockerfile
```

-	Layers:
	-	`sha256:e8aa42f4ffccc5f8c5c19f5e5058c2ba4dbe2927dd1ecd3022c6c40cea93c05d`  
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851452c4742f43d72b47517aa649b8dabe50ed847fc6bb02d0dda1f097697c17`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:707f5c087531fde2fe4cd0fa3a125c7467e99b7f6282a3e6ed338604aedb8c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-debian` - linux; amd64

```console
$ docker pull mysql@sha256:40925488baf8d5eac689f01e2659e6cf40b4b3bb3c244bba0ba21bd482fdd4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183452646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5aee5818e82c7cf5ff947329e5d962dd39fe020a4ef1e7442b52503918ab16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:26:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 13 Jan 2026 02:26:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:26:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:26:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Jan 2026 02:26:49 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 13 Jan 2026 02:26:49 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jan 2026 02:26:59 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:26:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 13 Jan 2026 02:26:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22e1a2160f42b051b03385b84706675799af27ef1d739855ea53e86c1db3754`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9018174d359de6a5328223860c685beff628396b4c0751bddd67bb6f436fba`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc91177be4b5ddabf028b6195345d9f121dd74538248e72a22d10a6bd5a4337`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 1.2 MB (1248687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba707135653628509d4c84f1cbe8c4a2cdd97b36d775765d7fc9f2ca48424385`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:22 GMT  
		Size: 15.3 MB (15295770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe1cdeaf5edd760187d6513d256abb23908c164f4a38247388365eea86f5ef`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9fa428fed3bfa308b0a3205123630fdecf4189ddab8c0c3603184bbf94f36b`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fcdfeee6d72380d9c3d4a00158cc023cf4e8540b36d9c4024d2fd4964525d`  
		Last Modified: Tue, 13 Jan 2026 02:27:25 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:23 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:fb4276d47d3a8247eb6723e1cbdd8e5efe29cce9d80ffbb8c7b008535c4d5771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d4fa1a08a98e8b03328728bb4292e3ff94f991594a62e81e53de38cd3d68a`

```dockerfile
```

-	Layers:
	-	`sha256:e8aa42f4ffccc5f8c5c19f5e5058c2ba4dbe2927dd1ecd3022c6c40cea93c05d`  
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851452c4742f43d72b47517aa649b8dabe50ed847fc6bb02d0dda1f097697c17`  
		Last Modified: Tue, 13 Jan 2026 02:27:20 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:9c3380eac945af0736031b200027f581925927c81e010056214a4bd6b6693714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7878bec832c6be5e61c39d3949651be8aa977daf875089b4560ae1434d2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232096327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e645fd9ffc4fc6745702d8c0068326b8707251166fdf11c80e8f52a609d19d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:27:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:27:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:27:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:28:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:28:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:29:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:29:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:29:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bcbef3f907005c3fa9c593eb817c5154fb78f135362c51ef716fd1edb703d`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee3c6664fb8f26a9773c040a58eed56426627b46ca63f824062a5626385d01`  
		Last Modified: Fri, 16 Jan 2026 23:29:42 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa0f442aff3224160d0d8ec20a5c4d106a3a9b8bed0ad66ea484fc86cd9c1`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 6.2 MB (6175177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7ef84dcaea1d1445baf02cb645626edee81b7420e8c22787d370c7646e8e75`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e06a2cd88c57a013246a89fda30e5b71902ac0e3e086432ee83f01a108bbc`  
		Last Modified: Fri, 16 Jan 2026 23:29:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bab8f9c85f0acaafe3a2c077e0a56304cc3c808111823e37060c9476d681a5`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 49.9 MB (49918398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655eb0dfc8feb1a31ee56b7840e34625bf54dd259a346b81a10fbfd99b39a121`  
		Last Modified: Fri, 16 Jan 2026 23:29:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae3e76dfc984a8dd17ef9c33be1fdd3d6b3794e3e24a39fa3f154b03de8623`  
		Last Modified: Fri, 16 Jan 2026 23:30:06 GMT  
		Size: 127.9 MB (127895065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a161f487a9a091587a3b55cf9351985e4936287c6576caa5aa4e4b1094c5f`  
		Last Modified: Fri, 16 Jan 2026 23:29:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8a12fa4e1d7896486f7fd81d83a1faaf36fc6e782051f4f0d985de43b52da`  
		Last Modified: Fri, 16 Jan 2026 23:29:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f7bb58291296cdce090c1c9a25d162c6cc8362ad60c4951f4630196fc74e65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5c1fca5b48359062429abddf7d66c7818c1c65ff1c3193e99a7f59fe50093`

```dockerfile
```

-	Layers:
	-	`sha256:b622c0882d0e13035a393c758180a1b09d5bb76758810d379a05d1f8e5c18040`  
		Last Modified: Fri, 16 Jan 2026 23:29:43 GMT  
		Size: 14.6 MB (14620437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2108fc02a60485aca46039e6e08ddee03d1a7af329926636c64360209143a55`  
		Last Modified: Sat, 17 Jan 2026 01:02:36 GMT  
		Size: 34.9 KB (34908 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c4989e05aa3ceb8cb6eb8a1b1f38ffa361eac2fec96ec67705d1b21c6390527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e501eca15118bb26fdb8fc5e0dfce27f687a2323c465e2e8cfe04a8221355ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:30:00 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:30:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:30:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 16 Jan 2026 23:30:26 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:30:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Fri, 16 Jan 2026 23:31:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:31:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 16 Jan 2026 23:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954bf984e9bf2c04f9107f437047609df0f9eec9d2f03812dd16e535ab586e4f`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a93133f047f0e202f0077f8e1c18d43d687442c00a6889ac10dd13bd80f0e4`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee9fbe69ed5f03d349f55ff723b007e3d44ee871c5fd2ca6a2ebe6ba308d81`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 5.8 MB (5798012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13baec4f8bc9cf19cb82937ea5750fc276ad2cd4ba1401964e67070d05b146`  
		Last Modified: Fri, 16 Jan 2026 23:32:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba93a33f57e70fbdf269e705f9a2f790269b60bd9a8facf607cae7735e2ace9`  
		Last Modified: Fri, 16 Jan 2026 23:32:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448975551cb36a03abcbffe5d99dea81800700c9bf639c0bf65e3aca5d745db8`  
		Last Modified: Fri, 16 Jan 2026 23:32:18 GMT  
		Size: 48.8 MB (48779290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e097ce1d0c9336cb62877d4dabb0f54d935908ca37a7b3bf334f7f4b8c0f5`  
		Last Modified: Fri, 16 Jan 2026 23:48:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768353cd89add26156537406cbb2b041e17b79ca187d6c0a6ea6198fe28f0c29`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 126.5 MB (126464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfd6b3b2078041085a5585a3c001c7fc3ea78b8aa5cc321bf4dfd8a9be0c2b`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145e7a1ce6315c068ec7baa6142a98a051bb37452614dfe41fd5d193666ef740`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:628109504e2562b29cebcfbff11c7f6d45cf6b00b2bf240822fc820984ea8149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b3388bef9486c455c8ff8168c57bf55e592511ae7f2064aa836df68bdc23`

```dockerfile
```

-	Layers:
	-	`sha256:1c77537a0f6d7d7c8b67e649f0352a0280c527807c058a4181e7310bab2bb0bb`  
		Last Modified: Sat, 17 Jan 2026 01:02:50 GMT  
		Size: 14.6 MB (14618785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e74b47efa6e5340638a16240548a03cdd641b0e9de0e0128098654614e107e2`  
		Last Modified: Sat, 17 Jan 2026 01:02:51 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4-oracle` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4-oraclelinux9` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4.7` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4.7-oracle` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:lts-oracle` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:0426ec38c7a10aa45ba383887df7878f74ee70e2fd589c7b69207f3577901903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32417d60c256a66828d3cfdc9ca9244576811a840000536e9a8d11c23e5d68`  
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 6.2 MB (6175148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25809bf57a8f169efb1bbd6588c1732f4f1836916ace0b507a4fef3dd158bfb4`  
		Last Modified: Fri, 16 Jan 2026 23:28:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13420727c1c0c0e213907e2e6267a5974c8c3dded97de2a95207f357668a52f`  
		Last Modified: Fri, 16 Jan 2026 23:28:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6e8ae58e2456042811ffa3661febd52abc2c7761443b2213c52bf6a56e469d`  
		Last Modified: Fri, 16 Jan 2026 23:27:53 GMT  
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

### `mysql:lts-oraclelinux9` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 23:27:51 GMT  
		Size: 14.9 MB (14897258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa111391adf2a8236c93d7b80ad95600395c646f74bed884c95f212dfe1d5eab`  
		Last Modified: Sat, 17 Jan 2026 01:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a139db383dcfd82710bfab9154fec7b22c1598706cabfb21480997ab9f09f`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff917e53173311673a78eef92f68b58006c7d241f55c90c063ff5d35f9b5f80`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7057a5a35be927e2eee436ccbee6ade905cf2905e0ded231f1eee51dd537d28`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 5.8 MB (5798058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3050ea2531d36b577b983be8afb48eee1fe18fe044013308e8cd5bb8d835a`  
		Last Modified: Fri, 16 Jan 2026 23:31:35 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37938fa9ff7d875ad4ea6b70f7fe1f112527c6ea161c7ab4b6a17b417591da1`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655cab6299cf71d7e9c2b44899bf9bd147d252fd3a35fddd6d22b99ddbf324a`  
		Last Modified: Fri, 16 Jan 2026 23:31:52 GMT  
		Size: 46.7 MB (46691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fec303eb563de541b75b7ea0dfda5ea894d8827ad63d4e61a2b23b2f7db927d`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b56d2ace31229a18ebed0f0205fab2b619aa2666b2af3e52520b805cb0ae6d`  
		Last Modified: Fri, 16 Jan 2026 23:31:40 GMT  
		Size: 129.3 MB (129323901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e151e2f48537d7e373cc742a1feef8240ad319f811917e7c8ffe31da18ba8d82`  
		Last Modified: Fri, 16 Jan 2026 23:31:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 01:02:37 GMT  
		Size: 14.9 MB (14895678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21660c0a2842109c3be55e8454bacac54817f6f768500373c4cef54317156538`  
		Last Modified: Sat, 17 Jan 2026 01:02:38 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:57c892ddeb17e6c7dddf219914db017b2cf3e2797806a75424444b83622cc8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00f711aeca86bf8a3e0e6dfd44f2a2b76014fc5fb59eda6c16cca3d692078d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2150accc6e3f548dc144e1e9aeecca8e06eaa5eb0f0fde96013dec583e13625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:17:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:17:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:18:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:18:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:18:29 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:19:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:19:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:19:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3687b576e09030d0137b68778ac8b794e931d12c86233b9a846bed3e1cee7`  
		Last Modified: Sat, 17 Jan 2026 00:01:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d39dd8c3ecec5a4aa482ea82cbdd336bdf0ccc5e9fe97857acc6f19f3061d`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cc70f011730a52b024ae2217527eaf26f9627e76590a5236d1381372c1463`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 6.2 MB (6175172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b569d93fe587e6f7fc6d4d6f8653ab0662793b182ec4d3c2f7915720c9395b`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3b86c4294968844915992442cc209a431158244998ffda17ffadd9a115cff`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29dc23d7bfcd16f0b280c416002d296812d269a41c7c914c2d6a770e9622ba5`  
		Last Modified: Sat, 17 Jan 2026 00:01:26 GMT  
		Size: 51.3 MB (51337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf0633cdd1831a67a9dd9e767018829498f2a3e4fa8023f787b70fc5147d65`  
		Last Modified: Fri, 16 Jan 2026 23:19:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6278c3f9bc1393ee533135a2366665f8e05f4006e5d80fef8f27cf4bac9a7f3d`  
		Last Modified: Fri, 16 Jan 2026 23:19:51 GMT  
		Size: 169.1 MB (169116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb9df71aa98262f8a9b94308790682229f0a9a4662169d4a7deb49ffef53e1`  
		Last Modified: Fri, 16 Jan 2026 23:20:04 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e9f880b5c30c1ed1e434f86aaf4669bb2b06b98209036a1a780dee6d316af0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a568dab01176bf1ac94375790d9b171339fff11f5149e5be36d707622190f8`

```dockerfile
```

-	Layers:
	-	`sha256:30c78be3a8366c1d99d9bc3f09d75ef95f74e69bd4365c72f7c15df05d7d0f6f`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 17.8 MB (17811692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f586e520b7839e804b9bcb4824f426e7dd7a9f40dcb7ca1a739b05d56fb07`  
		Last Modified: Fri, 16 Jan 2026 23:19:46 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3427e5b50d1eaf469e858e1ac026d643b87b2dde1037c59d87bceb1751fd1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb20f25c17502ee290cf550fce4ae60f80647e14a2889841e0fdaf337b0bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:29:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 16 Jan 2026 23:29:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 23:29:03 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 16 Jan 2026 23:29:29 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:29:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 16 Jan 2026 23:30:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Fri, 16 Jan 2026 23:30:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 16 Jan 2026 23:30:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 16 Jan 2026 23:30:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924c82fbc82a9eecc1572df06a50145607fd242e5f1fb9439b05f8240bff09`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5892b8b345e3cb2c3ddcac58883355e6ed7137963e770d8be9966865b117a`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dd235a9a2a7e215341f6e7b49b32f597d401af25cfb2a3cff5a3d35f0e826`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 5.8 MB (5798074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d83c289fce8ad2b520678e01610240d31a47c14b78e71b915ac2ffd06186d`  
		Last Modified: Fri, 16 Jan 2026 23:31:18 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0743b28fcff60aeb4d6fa3b4e513a70d1c6f88e0b87b33650e8b8f79c0c93`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1761851302a3e2edd49ac48552aee144d5037d284d54b44121cf2582db8387`  
		Last Modified: Fri, 16 Jan 2026 23:31:21 GMT  
		Size: 50.0 MB (49960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e766303672c6740f7064ab2366ae746c37371b8f99fb0c5b2c2028d6629fc5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa56a3fad114533409ef35e78b8d1ea8ece781aab2d1b236105dc38f23dd933`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 167.4 MB (167389810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7933d1e6d8aebb094bfc24e0e8427937f35b352308579c048531fc30b561e0c`  
		Last Modified: Fri, 16 Jan 2026 23:31:29 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ba4120e2e4755e5c5e8df7ba5ac2224321201db0ec32bf60868dbb5fbefe0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea796dcb648beb4d659a8b9c8bba9692a1df9f7a83c9e57d6cf10fbcfc95d02`

```dockerfile
```

-	Layers:
	-	`sha256:605099f469cfd4acf5650903f362545b02a5810b5898ca2ef32f242d0931b34e`  
		Last Modified: Sat, 17 Jan 2026 01:03:25 GMT  
		Size: 17.8 MB (17806831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ea0327b00bcba62230558f1497b7bd5c252511f547e28fa8d5d889d86a9f1`  
		Last Modified: Sat, 17 Jan 2026 01:03:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
