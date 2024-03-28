<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.36`](#mysql8036)
-	[`mysql:8.0.36-bookworm`](#mysql8036-bookworm)
-	[`mysql:8.0.36-debian`](#mysql8036-debian)
-	[`mysql:8.0.36-oracle`](#mysql8036-oracle)
-	[`mysql:8.0.36-oraclelinux8`](#mysql8036-oraclelinux8)
-	[`mysql:8.3`](#mysql83)
-	[`mysql:8.3-oracle`](#mysql83-oracle)
-	[`mysql:8.3-oraclelinux8`](#mysql83-oraclelinux8)
-	[`mysql:8.3.0`](#mysql830)
-	[`mysql:8.3.0-oracle`](#mysql830-oracle)
-	[`mysql:8.3.0-oraclelinux8`](#mysql830-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-bookworm`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-debian` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:8660220f10a03e81055938f34a0ccdb3f3fa6c3b9a47e2dc49a6c4a5abe3d6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:15a3cebfbb49f1096e4d98125908f65db535974d15b85193a9fd4b52c8653bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174792135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ef21d6632d1d188690e7cbe2c493b186eabc81c135c76a62a1c83960ba1c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0dfd031fa2ea26c04852cbc3e3496332031c4bbcc6aa546b9fe9b9b676e117`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 4.6 MB (4607359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd262f474ec3ea938207893ff87ab58d02d61163763a97d3d5a6538a957435`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665a713d084c2c04b9241a291d71dc4c51fa7ceff9ba9ee2898ea178130df47`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 58.5 MB (58529689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f00ebfc82ae25505f30ccb76be96453c4819ef6e5f10d8f9ee5fc1251c2ce9d`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe1791ff5120f7d95dcff2868a86ac4196ff41da58163458862fb5452d6ff7`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 59.3 MB (59335228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad3f9b7ea3d4e10e13301c3766c29c489d98c35052e00482e657d3422df429`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:283265c19d1420a3f84ac02098c77137b1506c4fe2cb58da91f9f96f8ddaaea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c7bddffaac98e93dc85e5acf31ea872df8fafaafe8e645b16eeebf1aefbbdc`

```dockerfile
```

-	Layers:
	-	`sha256:6764a2cc2de04ea0b96b9de5152287429f76340769665bda18f266e58fc4f142`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 14.2 MB (14248210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77631bb2fd96515396b277fa0efdd928ca7f5412dbb057dcf10570770aa260ef`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:713009fa62661ffb7f3eba30ec769c5d3b90b59b9f066edaeb6a728b59eb6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178454920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0671f32abb2a203585a48e248aa85a824d7621b9cf748e91caf971156f2e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147f1c5cd54b219c012165e41921595e676570d8679ddfca853690df3568faa`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc58f9b1e8241705c8d07731f28c785f7fb35ad0ad4b2f95b2d1e65824bd5a`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 57.6 MB (57579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e96dee667bf0bc6cccc83ea508ef11a2387b78dc1fe2376fc764373841bdf`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d85f5accecdea6be1fdb50b4ad63d1a4672327da1475499c03d6895bc61`  
		Last Modified: Wed, 27 Mar 2024 21:58:54 GMT  
		Size: 65.6 MB (65582792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ab4623d49f68844379465837b1a27dfb34f2f619066b2424635496b7fd0`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c415556e819fbc5f3af12d2eb51bee0aee51ac7b92dded043cbda1ac37ce960`  
		Last Modified: Wed, 27 Mar 2024 21:58:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:708bd0dc30fa1d30da2855ad8e05ddf582d1deefe896eae205355c1e46d1e59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3fd302ccd0ee17b27fdb4f9742ea071a713683a6d273a7117f1df20eee0faf`

```dockerfile
```

-	Layers:
	-	`sha256:e68e9dc9723330caac23a8265c668fcc25c663d371105efb6ce8ceae1a54a96f`  
		Last Modified: Wed, 27 Mar 2024 21:58:52 GMT  
		Size: 14.2 MB (14246472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e0f76a8d5669ec3708bd4d5280481e9d539e131d9513c56746d85aaf2fd2dc`  
		Last Modified: Wed, 27 Mar 2024 21:58:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:4552fcc5d3cdb8cdee76ee25cce28bf60b0eb3ce93d25ba3bfff7a66bfdcdee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:7c1ffa829a16a30594f619f1a54cdbc1126b34457229e353b8167aee61644f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82563e0cbf18162af685bff03debc195b851c327c31163fd211c0144d3c1baae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc451c3fb5566058fbe50d3cea82008343ae2a8614244bd6f2a682dea17cb8c`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db534de989c8aef71dbd5bddcabf63e5a257331be69ed599150769ed4fe39774`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1ab6fb3eac55eb2385c0cebf445972d01d7d6ff2abb11dd3e85c78cd2ceb9`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 4.6 MB (4607391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18a374d12e635636554c1f857d2fd49eac6f2530a3c24d677ee0b51551bcb71`  
		Last Modified: Wed, 27 Mar 2024 21:51:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f4c3e8c034a475f2b66e8f50db8e7890d309bd6ebf178cb7be7b89e48a095`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79cbebfe62344d6007245a65fda4525a93d7088da3cf580aa98751ee4b36cf`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 63.1 MB (63093962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3549fdd67999fdddfe270e22f7e06d820dcef9e24a1115505abd9af521f5832`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08846a4ab7a941debe49759ea5a2915f7a49748c899367c948b1062d71a1cab`  
		Last Modified: Wed, 27 Mar 2024 21:51:20 GMT  
		Size: 63.4 MB (63418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bd453daf0a01004d7b8a8ff266c34f4edaab6ef6d162174124d7f5b4887c5`  
		Last Modified: Wed, 27 Mar 2024 21:51:18 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f9a55bffacec3264637b2dd8f3d351e1c1c5381f7243ccd85512cf44743cce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e65153cdac2d9397f1865810c2444d6d10303dff7aa0028a66d71895b4d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0d59f28804b98b6286b99a1d0b8f9434a1f6dcf108a990c208a34cace8088f4`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 14.3 MB (14251308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef6f109cd32e8aebc7f957dc66c704365f96b46612d8636222ffff7e4a9cf1a`  
		Last Modified: Wed, 27 Mar 2024 21:51:17 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7367f5e53c64cc6f62afaeb9bd304034f6199170fa1d85afbaf9f6c14b67116f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af1be3715e5c01bd08d27e6a417c582c803daed2710f23d831c68022716db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519fbc71d3a7aef83e0e59bc4f0cd6198941951d39c6cd78f5d0aaf39b73fa34`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543c786ec0e2ccb2f2f2478291092f85b2246e5970d0235572e0669abca08ab`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 913.4 KB (913447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd7fa1c4c28d4194d33b55576371b45bdd163948e03b25619459d0929a78c`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 4.3 MB (4296426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b531b9c23df04b355c5930372503ec0f299106d0ca92067979f2b16509d109`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e5727259af69fc200f7efed6fa4ac45154d9608ad0388fc467982b9ae6297`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ab3dbe89336b904873ff60d60d5c43b3a1849e9471ef8628bd12d7909d246`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 62.0 MB (62038793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0dad6b1598205d9eda04da58e5b6f2fdde14edd31e15b7b8e0bd4478fb26b`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b98fb7a66608d67aa08b8ac83ebd1d18fe09afebc211b5001c3be698f45ce2`  
		Last Modified: Wed, 27 Mar 2024 21:56:55 GMT  
		Size: 64.0 MB (64020961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e0edca2bb74f2529c9a7bf843b8ddb19cf38edb65544fb6d2b5462ac206d9`  
		Last Modified: Wed, 27 Mar 2024 21:56:53 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f6f9240899fc36611d76bd9e4d5046658cb3e8a2a3161b5524847beab88906cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1988bcb5907b3dee2a6b077848f3175aec64d60455dd1a679fd7b24fee6ed`

```dockerfile
```

-	Layers:
	-	`sha256:691ee8d401f28e14588576057651b487561c6b5fc6dc5c457a264d7a1c606472`  
		Last Modified: Wed, 27 Mar 2024 21:56:52 GMT  
		Size: 14.2 MB (14249588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd68624d1677974170446d3b892b2e0f447053ea66eb5e220d458dcb35082ec`  
		Last Modified: Wed, 27 Mar 2024 21:56:51 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json
