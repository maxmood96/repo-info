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
-	[`mysql:8.0.45`](#mysql8045)
-	[`mysql:8.0.45-bookworm`](#mysql8045-bookworm)
-	[`mysql:8.0.45-debian`](#mysql8045-debian)
-	[`mysql:8.0.45-oracle`](#mysql8045-oracle)
-	[`mysql:8.0.45-oraclelinux9`](#mysql8045-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.8`](#mysql848)
-	[`mysql:8.4.8-oracle`](#mysql848-oracle)
-	[`mysql:8.4.8-oraclelinux9`](#mysql848-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.6`](#mysql96)
-	[`mysql:9.6-oracle`](#mysql96-oracle)
-	[`mysql:9.6-oraclelinux9`](#mysql96-oraclelinux9)
-	[`mysql:9.6.0`](#mysql960)
-	[`mysql:9.6.0-oracle`](#mysql960-oracle)
-	[`mysql:9.6.0-oraclelinux9`](#mysql960-oraclelinux9)
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
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:50:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Thu, 22 Jan 2026 01:02:45 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Thu, 22 Jan 2026 01:00:33 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Thu, 22 Jan 2026 01:02:51 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Thu, 22 Jan 2026 01:02:41 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:50:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Thu, 22 Jan 2026 01:02:45 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Thu, 22 Jan 2026 01:00:33 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Thu, 22 Jan 2026 01:02:51 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Thu, 22 Jan 2026 01:02:41 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:50:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Thu, 22 Jan 2026 01:02:45 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Thu, 22 Jan 2026 01:00:33 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Thu, 22 Jan 2026 01:02:51 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Thu, 22 Jan 2026 01:02:41 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:50:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Thu, 22 Jan 2026 01:02:45 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Thu, 22 Jan 2026 01:00:33 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Thu, 22 Jan 2026 01:02:51 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Thu, 22 Jan 2026 01:02:41 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:0546f878adee48eef82ccf936fc8ff932bdaa180ee614a8043ca917533654bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:460961fe4544452cdfa070f0c02f539caac45e8c0ef85bec8efe9e0ce5b4f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6151196d86929e6cc12db76c163bfd2c8c3a46093e54aae35e33faa552f8600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:48:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:48:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:48:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:48:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:48:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:49:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:49:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409234a5cefe2fb15fe401164c9ac5b83ce95bd4b09cee6e48963127d1908310`  
		Last Modified: Wed, 21 Jan 2026 22:50:30 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d66b5fe48e32a6037c3570d159cda17fa1afbe03ce237c983d21f663d4578`  
		Last Modified: Wed, 21 Jan 2026 22:50:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354993a02b40b2d67657ee1a468da0103d1bc049da7aeecd60470fb9dc92af8b`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 6.2 MB (6175151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a530771500dc6fe7e1aad497d69e3213de7d03e43abf5dddc04a29abcfa246`  
		Last Modified: Wed, 21 Jan 2026 22:50:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe8d818debcb9b265f173441d9a19a63961d16d7ae7e603e90bd6daa6c32de`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0022a26d15646a41c4e47b252c30307fc3e2af5fa2f52357962f0990665bf5`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 49.9 MB (49921847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350cb04be9532162d58d210bfb0313afc243ec841ccc8381890cbb9ede0191a`  
		Last Modified: Wed, 21 Jan 2026 22:50:18 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f93410f22da9c8d227162646f54954f723267305f5377acfdc577aec35c5`  
		Last Modified: Wed, 21 Jan 2026 22:50:21 GMT  
		Size: 128.1 MB (128105197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c271a9ab70e32b62237ce4e7eff3f8f39301ebb3b357ba80fc1fc37721793f8`  
		Last Modified: Wed, 21 Jan 2026 22:50:19 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777a18c49adaade43e72b4e9860d6000b26c2da5685e1ebf6695d78181abad3`  
		Last Modified: Wed, 21 Jan 2026 23:41:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5389b98483e1a82accf84083a8c9acc91fcb6239c9b4860b46ea4e4d6cfc0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f155d71544aef0dffae17723f733f14582836df9c9565ac7d0e4160e3fe6e10e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2feb98a44150c3128c6d6c6610550e5a5a523f36855810f8e68a28c8d4d8cd`  
		Last Modified: Wed, 21 Jan 2026 22:50:17 GMT  
		Size: 15.0 MB (14957469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3a6aa3235d67ec781fca23b912d616039b9a4e7bbfe36b49eedfa19ef97fcf`  
		Last Modified: Thu, 22 Jan 2026 01:02:34 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9126de385158d58a48c16a51474d4ae393c72f8ac26c030565703a64d856f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227909911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c6d6610e15363dcdfc49ee2f3e714f8be762da94bf9643adab4db5801da96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:54:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:55:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:55:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 21 Jan 2026 22:55:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:55:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:55:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:55:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:55:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb847422b0082b0709be7d2d5f4a5726b9b5c4a2a40847524469dcce22244402`  
		Last Modified: Thu, 22 Jan 2026 00:44:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8209f6c14b4b2384fd5d28fa43fed6e73988ea0ec2bca9362aaad9d20765`  
		Last Modified: Thu, 22 Jan 2026 00:04:34 GMT  
		Size: 48.8 MB (48775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c37cb44b415fc33301688a2954b8a6313734bc1d0190d338ed29c167d03c3`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b491cd47f71e14001baa563cefa9d45e1a3af0d014330e8111af0a8c9a0e1`  
		Last Modified: Wed, 21 Jan 2026 22:56:31 GMT  
		Size: 126.7 MB (126687408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c384409bafa51a7ba022ad8d497c0914cf0effd28b7879b7493e5cda03467`  
		Last Modified: Wed, 21 Jan 2026 22:56:36 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79204f6a864d70bfd67c12c4dc0ea30963cda8038e537c67efb6d2ece443b924`  
		Last Modified: Wed, 21 Jan 2026 22:56:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3a97109abdf144da908b21bdcea43594c5be723811a598348d1cbaae43787612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2b06a62a7ec21f1cb980f28ddc989205d821c316df8149852695043bbd9fe`

```dockerfile
```

-	Layers:
	-	`sha256:a6711f704c0dcc92e2db5bf258f5ff5e437513378478b4148e7b082459e9b2b7`  
		Last Modified: Thu, 22 Jan 2026 01:02:49 GMT  
		Size: 15.0 MB (14955817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69647a8f6141bacab36de64a49c30f6b61a01c5a0c7ddf51539c67e812448bc`  
		Last Modified: Wed, 21 Jan 2026 22:56:26 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 22:49:48 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 23:21:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Thu, 22 Jan 2026 01:03:09 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:02 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:08:07 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 23:31:26 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 23:31:19 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
