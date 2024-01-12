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
-	[`mysql:8.0.35`](#mysql8035)
-	[`mysql:8.0.35-bullseye`](#mysql8035-bullseye)
-	[`mysql:8.0.35-debian`](#mysql8035-debian)
-	[`mysql:8.0.35-oracle`](#mysql8035-oracle)
-	[`mysql:8.0.35-oraclelinux8`](#mysql8035-oraclelinux8)
-	[`mysql:8.2`](#mysql82)
-	[`mysql:8.2-oracle`](#mysql82-oracle)
-	[`mysql:8.2-oraclelinux8`](#mysql82-oraclelinux8)
-	[`mysql:8.2.0`](#mysql820)
-	[`mysql:8.2.0-oracle`](#mysql820-oracle)
-	[`mysql:8.2.0-oraclelinux8`](#mysql820-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
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
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35`

```console
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-bullseye`

```console
$ docker pull mysql@sha256:1d9f393d115c41a382a1f7d8dad5c073f0809739525ce501c7bbe45b0d2740c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-bullseye` - linux; amd64

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

### `mysql:8.0.35-bullseye` - unknown; unknown

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

## `mysql:8.0.35-debian`

```console
$ docker pull mysql@sha256:1d9f393d115c41a382a1f7d8dad5c073f0809739525ce501c7bbe45b0d2740c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-debian` - linux; amd64

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

### `mysql:8.0.35-debian` - unknown; unknown

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

## `mysql:8.0.35-oracle`

```console
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-oraclelinux8`

```console
$ docker pull mysql@sha256:82b40099c780c15850690bea3a76c73fcc4834ce813313cd048468f1de7c2b06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:3a0b76a2ee46a23fc8e0c5e2d38d016a8466bbc774c933d719ae0b5308982dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048db12589d011b77ab3ea33b7010d0b549214c8baa5fd885e4af84887928f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95fc125cf8067473c7c0aeb06cc55f45268807b23568fbc3f14cab35d285cf`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22412d6d690fcd08a40e3808538b28c8ff614ca7d4292b97f91862c7d90f8279`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d453aad0ebfa3f5472ee10df0b3e529d95ea63518574c69ceb52f5cf22d4c4`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 4.6 MB (4594897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cca7a391de90190ab3ccfd94b95a59a48c0622005d5a5f5f364ac0c4c02e0`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7ae94329772a89c4c8e768d2f2209b96d4573ecf54dd50a679ddcaab6ec64`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3e28b094a2e946679cb3f91d09922e2ae80bc117e6c3dc52016468e77ff1c9`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.5 MB (58505933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db237bdcf1c0c61bb338e11bec6ba80c30afae0097636229de54a52fc9b2b41f`  
		Last Modified: Thu, 21 Dec 2023 00:42:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c3f5cb4f4c88a98466d248ca0027a0abbd6d6301f0d166bd925eb58cf5ebd`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 58.3 MB (58312328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394dbd7e05eb13c1f4b395b558b1c40b708996f1c5eb5dead40242895ce31121`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a167e598b07c1067ec74fb4f63dd9a06c3baa1b6923afe66cfb4911c76632f`  
		Last Modified: Thu, 21 Dec 2023 00:42:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:e947f8eb99f01f51bb4a1a0506f0a5e23e03b48e78c68fb4931232b92bc96154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c396d9ca70fb4db2a43ca8d5ce6ab8de931e72363589fd41c168185836c0988b`

```dockerfile
```

-	Layers:
	-	`sha256:e5579f8c4a1d658618ca9a6429cc1f69801c829936675aed2b3837bd7b03ba46`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 11.6 MB (11568051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65568400f27660daae64a470173a41ed0af8ec67a24a230eae4e6ff1d0a53d8`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:95eced7eb7de7a1ae4d4fce22f69dd8eb656d221955d386c2b08882ea77ff7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fb4b5cf6c7d697a7ae7e7ef2e705377e95cf7252f943f63ce048f01e4f668a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c780b07b462448b0aa43845ba1938d9a67b94656112b1bfff0f0d1ea379659`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7e4603d80c8907a1f978a60b8502992692666e4dd5ee73048d522aa43161e`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 57.6 MB (57571915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019028606eb87053ff691c63b6791d8d97f2a67c05cda35892e6b9a1f4b85ba1`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654218039fc54e07e6c78e94c2263f57706edb4079022f4c421926cd8c5d0fcb`  
		Last Modified: Thu, 21 Dec 2023 07:04:38 GMT  
		Size: 64.6 MB (64577803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2374d716b2dcfa86a0a2549336e968d1bafa878b9e07635bd97c61ae6426e`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41834b272a83660da09733a4913e23e17e8547bf9d43976d32d4caf02ae82831`  
		Last Modified: Thu, 21 Dec 2023 07:04:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:9b930dae5a54811ffaba918c45c276d81b2a7e2f12ae58d17ddb28bb6c9a78e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d4136e0fd5d4a248bdca8e83b736ef2a88a8e4b7921646994a91d3c501c77`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef81bddc411899408ac99d460d5bd396674b84d813bdc14499488fc218773e`  
		Last Modified: Thu, 21 Dec 2023 07:04:36 GMT  
		Size: 11.6 MB (11566631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84aec4d2a48e9364f6362c95c0f7826c4f7cb78ed50a359e2efa10e34d0ad2b`  
		Last Modified: Thu, 21 Dec 2023 07:04:35 GMT  
		Size: 34.4 KB (34395 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oracle`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oraclelinux8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oracle`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oraclelinux8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:4ef30b2c11a3366d7bb9ad95c70c0782ae435df52d046553ed931621ea36ffa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:28a16e31b140d750048cd5fadcaed22ac08d0eeb18567f79f822aee1f237b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181572393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246731c4b01c19b8713c6408c6c5d898ac04f75f2a4ce998930f12091542f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7e9f463619cbda1168fb597e71ce50b4ecd4546ad74050f5b5c67a152ca249`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f403783c74e137d330ef98facdded2cab753187765ed8c453bb7b061a0002`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e53a613d8011ad3d6207863d1555fe571430d3c6f7659d1eb0fd7f28ba7de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 4.6 MB (4594819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a362044e79fb6669726216e996a0a9fa018ba304d75ac30c9378a93160182de`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4df4f73cfe883156b974e5269c673e52de0e1a56d610f2974793cd52d8b043`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69263d6347550e51a3b3f972d5aee303fd3c8c6d75376aad0b4cdcd4cb3f83be`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 62.6 MB (62574253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e855492024c60c48d8eb006c94b71d6622f6d5c741cfa611e571a88a67d37`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02229ce6f164ee6c47c91ddaa42db249b197b8b28dc6814a4df879a4f96a3e`  
		Last Modified: Thu, 21 Dec 2023 00:41:50 GMT  
		Size: 62.1 MB (62087711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320aa32bf42c0642bc86e30dac0b10335258a24b6ba374e173918ba8d9f9f63`  
		Last Modified: Thu, 21 Dec 2023 00:41:49 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:483bf8eb111365bf322a25443d3f96ae0d80829c60f00fb329d8a0de0f21c6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11608021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f9b1df36151d7e7ebba69fac20d69995d956d3851313ac3b4fdf9fa4e9ad3`

```dockerfile
```

-	Layers:
	-	`sha256:8de9290b82bb48a07e68ea96148c288ffa09729055d5c506b7690cf42f948baf`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 11.6 MB (11573114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a63c307592189c7a4ea188ee3b5e76eba99edc475a34c635157d5e893e536`  
		Last Modified: Thu, 21 Dec 2023 00:41:48 GMT  
		Size: 34.9 KB (34907 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e870e58e0e1f937652982f99cddff85ab2076d217db08732856d22eb334e9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185267811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e409b83ace60740ab0396735db367d86956b860af922e9e8e5116d9113714a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
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
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347407baabc139352e501ab8b38535ca241501dcb8ec03a1b510c48073a44dd`  
		Last Modified: Thu, 21 Dec 2023 07:02:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2468bda244ecd5eb95e34adb03d208c7febf9ae674b87d5d8e47a95e7e60d`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f773ef2c8719129309a953575ab852004987e1f5d633bda87e9e39adcdda2e`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 4.3 MB (4293519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad2c7f0c6a3a98d7135f356143c3b2b8ea49bb3f44929d919573e6fe1bda90`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808b6b0a452fc574751c81e66977041bafa31fd9b3f69fcbd27b93a225e0270c`  
		Last Modified: Thu, 21 Dec 2023 07:02:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938c61da20f1c72dac798ff747f1dbfdc80f216e907aff5f218f6a83c97c677`  
		Last Modified: Thu, 21 Dec 2023 07:02:50 GMT  
		Size: 61.6 MB (61595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b3b553e4fd8f980136a477d9578009c0db85f1db25e7b1fd5420c5d8481c`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ae17e153b3968dec87a4940228bbad947809e4fe38edfeb5d5743177c164a`  
		Last Modified: Thu, 21 Dec 2023 07:02:52 GMT  
		Size: 68.4 MB (68377005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29255c8a5cf0c1efe1c91b713f6a22ba490a922f419938ac123caf9bc3b8616f`  
		Last Modified: Thu, 21 Dec 2023 07:02:49 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8bfa6bfda24cf129ce2a20ea3fe679ad377840c0c16d7937887233485b3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0090c5fff9832517cfb17c9b11212808566fe58c5de5cd3c0b0caa8b3853c3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe71fd1f4151b9017635d498f57dfb6d6b932f909c21a79cf1186851ec3317a`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 11.6 MB (11571712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977332ebd0a237ff1a892785275d5af61c13b24cd15cbe0ed7cadb7b5b68102`  
		Last Modified: Thu, 21 Dec 2023 07:02:47 GMT  
		Size: 34.9 KB (34939 bytes)  
		MIME: application/vnd.in-toto+json
