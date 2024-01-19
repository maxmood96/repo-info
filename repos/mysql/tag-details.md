<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bullseye`](#mysql80-bullseye)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.36`](#mysql8036)
-	[`mysql:8.0.36-bullseye`](#mysql8036-bullseye)
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
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:c6812f0dcd978b589d9d3b90c20bd5e4a799deab4fd492985e0a076c5be1ee40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:82d43fa55566029f346be6f84374c886ab78f3d390821811434aacb0051a8bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173695177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f16659c1292812cabe673478e558c1e57a7df5710c232d825e49faa15e7b40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ede9724f323747afcfac611fa552b6c6871710b4ee7ffbe8e7f2305253580`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46e56c49748ad1ef3df50f592b21e93da8451f776929834de185f6217def34`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d2ee58a8b297e70da0f9c5d61124cd5d38b0af4275a8da0b4eff5cba8e9f7`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 4.6 MB (4590728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ddae3eed3d8ad92e17c90267b865dc75641c163870141934eae57e2d7285`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8240b5bfd24daf36a68f13fb8a3f19273398338db34b4fb703f02fcbb73509`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ed96f802c1a05151b8a24d09d241aaa647817b583e84cc12afb07f38b5eed`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.5 MB (58499707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e7675236c28f0df7dc85a75b4802e75e92127d0baee61e296ff5e11716b7d`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e76090f013fd817670395e56996ddb377d16151cb9557070aca9ca2a51df21`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.3 MB (58290760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d100781ccf966bfe70e456467538ad727ee52085bb89d101293f1232be55f63`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011afdd7e19aa51f6ea1b97a4d4012a5db71d3be213fd26c858666789a9ff1b4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:edb6603b673a1da322ced648665c9c2295e4adcb6064149082df4d0a8f275525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e3d9157a741a8451aa64b32feb9850d3d6a313bf9bae71f5f9a2137cc3c00f`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b821e22307124750d91ad6882624bd18ed8598fcc79ea801218be21a2a76c`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 11.6 MB (11568059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e79a6f8fb8c1bae84f303ad2a0e72a56e8568d9a327e814e72c4c521ad775fc`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6daefd90d20539731f42bbaed66aef4fa8aaf5e975ae8cb5ce1bce0e08483f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177475891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af4f25001c5611cb1449bb3610d2c341b115d099e87dbcc8444017e38bfe45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973d772a17e3dad43aec9de4c3a7dce27288b55b6339629b14bd24010b24d21`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9a6c2ebfbd6aea57d93eafc4123d1740cce81808acba9a5d85dbd8880663de`  
		Last Modified: Thu, 18 Jan 2024 10:41:12 GMT  
		Size: 57.6 MB (57574816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b79f7fae5277114d8afeb416c72180f3e640b5b9dc2e6c94435e442eebd6c`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76607ddddc68d59bd1ee822c12571fac6d827e82b2ce0405ec6b03ed0afd8cc7`  
		Last Modified: Thu, 18 Jan 2024 10:41:14 GMT  
		Size: 64.6 MB (64595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d9daf91fd05c21c36e5b4845b8f0840cd0dc54d88e0623e9d6771db623b052`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d374d01142d1b07c0a4a777fb3205abab720cab3fd6cc8924a946f408f4987`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f657a62885ad3b55f08856bbd31e498d22b1ca690d6dacf7efe4333cd5592d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f45dd1db4f69efdf9760fe89534087f613261b7d9c1232f6076b34d1ad61c2`

```dockerfile
```

-	Layers:
	-	`sha256:dd6debea0b4b2c8d67f7bbfbec733d8c973b770115a1c050568b75801bdc4367`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 11.6 MB (11566639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cf71fb4eebff224f24e27f7288c9269db0b24b76d0184378995b67eb32e56e`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bullseye`

```console
$ docker pull mysql@sha256:1d9f393d115c41a382a1f7d8dad5c073f0809739525ce501c7bbe45b0d2740c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:0b05121ef586864f54eb63f285c9d8ee84cd36bf160ad3330c9e39cf384bdd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179125891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edae131fea9931df7b6d3d95ba63bc556e74d778bb17e2db173a460774f7deb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Mon, 18 Dec 2023 23:06:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509e99ccd909e6cff58bfebf07d4aa9488751c812eb4942c6162318133c16c8`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18449158c1925dd80875324d6569ccd77dd7508df103db08b1b1044cab64a8bf`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 4.2 MB (4207433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4838008371a5f6eb05c3de82aeec5ec59eee141bc710db552c11c7f136c5aa9d`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 1.5 MB (1472425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a500de9e6c79d9df638dd56687bc372c51258a8f30664e7f3f9d5df4bfbc2`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7788a0cfe39d71e7c76d4f5357b07cf1cd33a8f2f726ba980c3a125ba9a7676b`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 12.5 MB (12454952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d82554e9050b5a36796abc5036ef507eeb5d6ef972e45712059e74068677d1b`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473684d155cf497a12db85f2a6d6e4803909bc09a6dff98a102b633538c92098`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eabb9f2adb1a6659cb13f32839a6a85b37bf47bda04f945a66e7749856fda6`  
		Last Modified: Fri, 12 Jan 2024 00:22:41 GMT  
		Size: 129.6 MB (129562486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80382a09301fb5162ccba05e694537807d9c820819e45aed2c7116aa4b556156`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b929280da2d3a9f684ab8d6c5a507a8eaa084d46438da16dfcbfba11a457ca28`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a1df60142e3c991718fe72aeb0111667152aa64ff82e94d3c6e1ab7cdc8da`  
		Last Modified: Fri, 12 Jan 2024 00:22:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:1d89399295f819fcf0fa0aa4529ea628e4bd6a38b7a14aff0774f8f05f1ee22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaf4f76d2bf9778ca9ca651decef72d096538812c496628b451810e9c827f34`

```dockerfile
```

-	Layers:
	-	`sha256:82a57a8c5e0c4b23df3e4bf7fb4e1dd9dfdd0131818b5ec97ddc712ecab1a2fd`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aad367de4cadccd1d0aa21a37e8376d469c27b39e0abc6ba0cc6a9245a45920`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:1d9f393d115c41a382a1f7d8dad5c073f0809739525ce501c7bbe45b0d2740c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0b05121ef586864f54eb63f285c9d8ee84cd36bf160ad3330c9e39cf384bdd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179125891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edae131fea9931df7b6d3d95ba63bc556e74d778bb17e2db173a460774f7deb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Mon, 18 Dec 2023 23:06:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509e99ccd909e6cff58bfebf07d4aa9488751c812eb4942c6162318133c16c8`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18449158c1925dd80875324d6569ccd77dd7508df103db08b1b1044cab64a8bf`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 4.2 MB (4207433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4838008371a5f6eb05c3de82aeec5ec59eee141bc710db552c11c7f136c5aa9d`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 1.5 MB (1472425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a500de9e6c79d9df638dd56687bc372c51258a8f30664e7f3f9d5df4bfbc2`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7788a0cfe39d71e7c76d4f5357b07cf1cd33a8f2f726ba980c3a125ba9a7676b`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 12.5 MB (12454952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d82554e9050b5a36796abc5036ef507eeb5d6ef972e45712059e74068677d1b`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473684d155cf497a12db85f2a6d6e4803909bc09a6dff98a102b633538c92098`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eabb9f2adb1a6659cb13f32839a6a85b37bf47bda04f945a66e7749856fda6`  
		Last Modified: Fri, 12 Jan 2024 00:22:41 GMT  
		Size: 129.6 MB (129562486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80382a09301fb5162ccba05e694537807d9c820819e45aed2c7116aa4b556156`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b929280da2d3a9f684ab8d6c5a507a8eaa084d46438da16dfcbfba11a457ca28`  
		Last Modified: Fri, 12 Jan 2024 00:22:38 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a1df60142e3c991718fe72aeb0111667152aa64ff82e94d3c6e1ab7cdc8da`  
		Last Modified: Fri, 12 Jan 2024 00:22:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:1d89399295f819fcf0fa0aa4529ea628e4bd6a38b7a14aff0774f8f05f1ee22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaf4f76d2bf9778ca9ca651decef72d096538812c496628b451810e9c827f34`

```dockerfile
```

-	Layers:
	-	`sha256:82a57a8c5e0c4b23df3e4bf7fb4e1dd9dfdd0131818b5ec97ddc712ecab1a2fd`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aad367de4cadccd1d0aa21a37e8376d469c27b39e0abc6ba0cc6a9245a45920`  
		Last Modified: Fri, 12 Jan 2024 00:22:37 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:c6812f0dcd978b589d9d3b90c20bd5e4a799deab4fd492985e0a076c5be1ee40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:82d43fa55566029f346be6f84374c886ab78f3d390821811434aacb0051a8bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173695177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f16659c1292812cabe673478e558c1e57a7df5710c232d825e49faa15e7b40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ede9724f323747afcfac611fa552b6c6871710b4ee7ffbe8e7f2305253580`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46e56c49748ad1ef3df50f592b21e93da8451f776929834de185f6217def34`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d2ee58a8b297e70da0f9c5d61124cd5d38b0af4275a8da0b4eff5cba8e9f7`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 4.6 MB (4590728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ddae3eed3d8ad92e17c90267b865dc75641c163870141934eae57e2d7285`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8240b5bfd24daf36a68f13fb8a3f19273398338db34b4fb703f02fcbb73509`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ed96f802c1a05151b8a24d09d241aaa647817b583e84cc12afb07f38b5eed`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.5 MB (58499707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e7675236c28f0df7dc85a75b4802e75e92127d0baee61e296ff5e11716b7d`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e76090f013fd817670395e56996ddb377d16151cb9557070aca9ca2a51df21`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.3 MB (58290760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d100781ccf966bfe70e456467538ad727ee52085bb89d101293f1232be55f63`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011afdd7e19aa51f6ea1b97a4d4012a5db71d3be213fd26c858666789a9ff1b4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:edb6603b673a1da322ced648665c9c2295e4adcb6064149082df4d0a8f275525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e3d9157a741a8451aa64b32feb9850d3d6a313bf9bae71f5f9a2137cc3c00f`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b821e22307124750d91ad6882624bd18ed8598fcc79ea801218be21a2a76c`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 11.6 MB (11568059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e79a6f8fb8c1bae84f303ad2a0e72a56e8568d9a327e814e72c4c521ad775fc`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6daefd90d20539731f42bbaed66aef4fa8aaf5e975ae8cb5ce1bce0e08483f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177475891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af4f25001c5611cb1449bb3610d2c341b115d099e87dbcc8444017e38bfe45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973d772a17e3dad43aec9de4c3a7dce27288b55b6339629b14bd24010b24d21`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9a6c2ebfbd6aea57d93eafc4123d1740cce81808acba9a5d85dbd8880663de`  
		Last Modified: Thu, 18 Jan 2024 10:41:12 GMT  
		Size: 57.6 MB (57574816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b79f7fae5277114d8afeb416c72180f3e640b5b9dc2e6c94435e442eebd6c`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76607ddddc68d59bd1ee822c12571fac6d827e82b2ce0405ec6b03ed0afd8cc7`  
		Last Modified: Thu, 18 Jan 2024 10:41:14 GMT  
		Size: 64.6 MB (64595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d9daf91fd05c21c36e5b4845b8f0840cd0dc54d88e0623e9d6771db623b052`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d374d01142d1b07c0a4a777fb3205abab720cab3fd6cc8924a946f408f4987`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f657a62885ad3b55f08856bbd31e498d22b1ca690d6dacf7efe4333cd5592d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f45dd1db4f69efdf9760fe89534087f613261b7d9c1232f6076b34d1ad61c2`

```dockerfile
```

-	Layers:
	-	`sha256:dd6debea0b4b2c8d67f7bbfbec733d8c973b770115a1c050568b75801bdc4367`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 11.6 MB (11566639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cf71fb4eebff224f24e27f7288c9269db0b24b76d0184378995b67eb32e56e`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:c6812f0dcd978b589d9d3b90c20bd5e4a799deab4fd492985e0a076c5be1ee40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:82d43fa55566029f346be6f84374c886ab78f3d390821811434aacb0051a8bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173695177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f16659c1292812cabe673478e558c1e57a7df5710c232d825e49faa15e7b40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ede9724f323747afcfac611fa552b6c6871710b4ee7ffbe8e7f2305253580`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46e56c49748ad1ef3df50f592b21e93da8451f776929834de185f6217def34`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d2ee58a8b297e70da0f9c5d61124cd5d38b0af4275a8da0b4eff5cba8e9f7`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 4.6 MB (4590728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ddae3eed3d8ad92e17c90267b865dc75641c163870141934eae57e2d7285`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8240b5bfd24daf36a68f13fb8a3f19273398338db34b4fb703f02fcbb73509`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ed96f802c1a05151b8a24d09d241aaa647817b583e84cc12afb07f38b5eed`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.5 MB (58499707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e7675236c28f0df7dc85a75b4802e75e92127d0baee61e296ff5e11716b7d`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e76090f013fd817670395e56996ddb377d16151cb9557070aca9ca2a51df21`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 58.3 MB (58290760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d100781ccf966bfe70e456467538ad727ee52085bb89d101293f1232be55f63`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011afdd7e19aa51f6ea1b97a4d4012a5db71d3be213fd26c858666789a9ff1b4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:edb6603b673a1da322ced648665c9c2295e4adcb6064149082df4d0a8f275525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e3d9157a741a8451aa64b32feb9850d3d6a313bf9bae71f5f9a2137cc3c00f`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b821e22307124750d91ad6882624bd18ed8598fcc79ea801218be21a2a76c`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 11.6 MB (11568059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e79a6f8fb8c1bae84f303ad2a0e72a56e8568d9a327e814e72c4c521ad775fc`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6daefd90d20539731f42bbaed66aef4fa8aaf5e975ae8cb5ce1bce0e08483f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177475891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af4f25001c5611cb1449bb3610d2c341b115d099e87dbcc8444017e38bfe45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973d772a17e3dad43aec9de4c3a7dce27288b55b6339629b14bd24010b24d21`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9a6c2ebfbd6aea57d93eafc4123d1740cce81808acba9a5d85dbd8880663de`  
		Last Modified: Thu, 18 Jan 2024 10:41:12 GMT  
		Size: 57.6 MB (57574816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b79f7fae5277114d8afeb416c72180f3e640b5b9dc2e6c94435e442eebd6c`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76607ddddc68d59bd1ee822c12571fac6d827e82b2ce0405ec6b03ed0afd8cc7`  
		Last Modified: Thu, 18 Jan 2024 10:41:14 GMT  
		Size: 64.6 MB (64595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d9daf91fd05c21c36e5b4845b8f0840cd0dc54d88e0623e9d6771db623b052`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d374d01142d1b07c0a4a777fb3205abab720cab3fd6cc8924a946f408f4987`  
		Last Modified: Thu, 18 Jan 2024 10:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:f657a62885ad3b55f08856bbd31e498d22b1ca690d6dacf7efe4333cd5592d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f45dd1db4f69efdf9760fe89534087f613261b7d9c1232f6076b34d1ad61c2`

```dockerfile
```

-	Layers:
	-	`sha256:dd6debea0b4b2c8d67f7bbfbec733d8c973b770115a1c050568b75801bdc4367`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 11.6 MB (11566639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cf71fb4eebff224f24e27f7288c9269db0b24b76d0184378995b67eb32e56e`  
		Last Modified: Thu, 18 Jan 2024 10:41:10 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.36-bullseye`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:innovation`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:212fe73edca5df6ff14826d5eb975c914bfb91f82a2e923f9050568f99525da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:5ba9d31938cfbfbcd6b29977181cfc246ce3f4b4923efc2af89c028d872fcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181549171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc861cf238f24a71398f27b6eb77051fe60b834e003f33e4a36e3e19c37df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b67b0dd6aff81c190da4012918bee8a167b30ff6af208b3a25e477c3ee291`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50314d46ce2bcc7eb441b7d8b73f0d542f71babfd69783084191ed7cb986d137`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494babc9226311b1cdb3c1bbde0566ed15b8cff7b61368bf360affae28e40b02`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 4.6 MB (4590747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02548e6f2dbfcde4fb252b2be5c9774d4e85549a9e7c06c29eb8057b462765a7`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e5e2637e0d574a25e97e904e376bbff5032bc479b018aee24cff78a60c3769`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b198fe6b7bc2a01e42dd907b6a8489d053104fb655184b4313489ae324cb4`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.6 MB (62570457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a2b0eabbf35b7447ec5212dc2f78db031e9b168ea5ef3f7e1aebc75c3ce95`  
		Last Modified: Wed, 17 Jan 2024 22:45:07 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a4c7a89c59ea677de13ff9b08f4ff4a83c2663dc551171122e907d2ae06fd`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 62.1 MB (62074091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe599fe218ce4ad0aa653323c1c20b55092ee35841646afbcd9aa8e4335d70`  
		Last Modified: Wed, 17 Jan 2024 22:45:08 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:dc1b710346fe9e1a9be6338028427dd3b3461285f4994303863615e22942c015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a61f1c67fa3418d79e71ae2e182bbd5ad414b2030bd9822379818b27b040fcf`

```dockerfile
```

-	Layers:
	-	`sha256:21067c97c3c62785cdca12bf104b49fe4f9dc0c29d8d065acbbaf32c980e249b`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 11.6 MB (11573122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fddf4967028167fdb6ec3f3c95189c3df7b82aff5679bf908fcda9ad8a114d`  
		Last Modified: Wed, 17 Jan 2024 22:45:06 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json
