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
-	[`mysql:8.0.37`](#mysql8037)
-	[`mysql:8.0.37-bookworm`](#mysql8037-bookworm)
-	[`mysql:8.0.37-debian`](#mysql8037-debian)
-	[`mysql:8.0.37-oracle`](#mysql8037-oracle)
-	[`mysql:8.0.37-oraclelinux9`](#mysql8037-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.0`](#mysql840)
-	[`mysql:8.4.0-oracle`](#mysql840-oracle)
-	[`mysql:8.4.0-oraclelinux9`](#mysql840-oraclelinux9)
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
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-bookworm`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-debian`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oracle`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oraclelinux9`

```console
$ docker pull mysql@sha256:5c26f41e64c9159b1c485182575d6ebcd607ebf65fe68a26a71ca241c7748377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0494f3deef5cde938c7a05d8702bcb03a5629120baf8c061fa1ae0e5128f586b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a835b8f8a3aeae7202cd00af96bdcb6bed31935466839940191367bd0f274b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d73c4ea50dc59c8fbc667fbfa8cfbeeb55d54c29489fa0523f19f741686a9`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df906719f48b8431c4b1d637b3bc8c1c4209a8c7ec21104790b62cd2e638883e`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a24902de261245eae689df876ad6029a22ff688240e6f4dcce0a901b1e970e4`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 6.7 MB (6711543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d013a8b3610d495b289e95b2240054b8251ecd26714e5aeabd63dd9031b8144`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb6650fbfc15368d135551d4793014f9c4fce821ae25dc4da8e019eea2a32e`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af49f0e308ba33226c7b9c4458248ea2d11522b8c56115569b3ee3d14d81197`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 49.1 MB (49147339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f748674a9ada89b9ed0cee4b0d42712fb7542d0ab76970472a5b1ba53fb23fc`  
		Last Modified: Wed, 19 Jun 2024 02:01:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b0d775db5c9ea9c94d9a7726ed5744cb6a8a955b406346f11eecf44102052`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 60.2 MB (60171061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fde0b059524965ee9309631d8f0c202cb3fe88509f17e61c9bf9476e7f26d3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98dd5f45e7cc16c10aa8fe9407e3997585f9b7eab742558f58f59a159d7eb3`  
		Last Modified: Wed, 19 Jun 2024 02:01:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fd4df0960e5656e984612a302af657e3d093f230e56c2a8c47d735fbdbbca512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea0418952103bb476043f376e24067c50703c5dea65a3a95e0b054a248d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d3d427f22ca3c9205e6f86fcdbc8d8227f254f06b6f05e644dbfd7d072fdf7`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0f69443172e612517f4f2731ed7f68d0029e9e120e0c767d36fe012b4beaae`  
		Last Modified: Wed, 19 Jun 2024 02:01:06 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ae4c48667d6ead1f3b63ec1a4887315108b524e0fcb58554019317c3f84ac665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170563226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcff079af180179a1b17408073e990378f4de745a841b094cdafc917a129be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b199ba2ab8cee71c058f397fc93e7073491f4dae56b0fb5f4ae779fb56fea1`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c67a0a4f456df2b1d5e3e30569e47acc9b2fee1de0c701dbe73953d6566259`  
		Last Modified: Sun, 02 Jun 2024 01:40:33 GMT  
		Size: 48.0 MB (48028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e6d184a5b7ba0a785418a656dad0dacf1f42bce11fa8fde1ef66d9b957880`  
		Last Modified: Sun, 02 Jun 2024 01:40:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a7281eee87feae9236acd35e5172aca0aff33edf220b1a7f040e4c4cc1f3`  
		Last Modified: Sun, 02 Jun 2024 01:40:35 GMT  
		Size: 67.6 MB (67647482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc775f3735831d9b775b6f225b0b449ed71b3b70ced03c49e957a125f9ca030`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32832d2ef9fe48efe65689ee34d1e648b9b5cdf9b44ad23b43acaef844caffad`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ed3434ed2fb8858a403302d5246f09021609a73897f7a3b5eb8612a24983afb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aafad644b0675fe846a8017a08b9cf3d859c56719140e708a4d4dcc2e4347b`

```dockerfile
```

-	Layers:
	-	`sha256:2de066f2346f1b7e269066efeacd06305ea1d1f83927864f494ad3929ed02d3c`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 13.4 MB (13444200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57174857034c2fe13ba8583d7203c72396990ec9e1fac8ccd853896f562fd534`  
		Last Modified: Wed, 19 Jun 2024 01:55:36 GMT  
		Size: 35.1 KB (35111 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:0ca0b071a08d5c9abebb9d4db755582ba5e0830c3723def877bc1ef223e5e482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b8aea6614f5c0bd76268933caa05f17fd847fdc89b4dc3cfeddd5dc9d7940f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f08c39533c7c7e6ffd10240490c1f915582a9daa53cdb1f4e6941616ed153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0483f77b9a6b3b02c5f2eb44cde4e8a25914914fb730963afeadae062d6088`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8d47a0073c02cf6529aea56e053ac2b64ffe10adbaa2e81f28c6e36b51cef`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c065f3c10d1a1300cd37a0f0144b203add7a4ebc4c957318719fbbf9dfe89`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 6.7 MB (6711648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a10948c748f0b356453388e3047f3bc70fdcf7769d354759738f0e6e9dc4c`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feac21ed6d69766f1ea9508a4fd976b2c05c38d44ee16f5018d895d3900e56`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d830e36bd72346ec135f728deba41af0dd398a035fd0a98a2f79813335f730f`  
		Last Modified: Wed, 19 Jun 2024 02:01:21 GMT  
		Size: 47.2 MB (47215082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372383574a399f6cc0f76b926177ab5000bd2c2c895fa80d0c8192694d129b9`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23825c9038f1ece5e550897f6dae5c9a9a7ceb19a3ccf959bf3abe7c76ca10`  
		Last Modified: Wed, 19 Jun 2024 02:01:22 GMT  
		Size: 64.8 MB (64786507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1b19781afc4c0c123b0428f15bc79bf9110873bc54e9d1492ae93496669c6f`  
		Last Modified: Wed, 19 Jun 2024 02:01:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:66f6ab6418906894fefd3980d35f71329a482a8f6b3f35b3fe651b0aabac144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217729306336bcee9b4293d2aeeb3365760eb1eaf7bd29c566ee906d876cd23`

```dockerfile
```

-	Layers:
	-	`sha256:03f50553315f20d5afe71a08932ad65cd2f230b42eceaf7944c686d82fc7cad1`  
		Last Modified: Wed, 19 Jun 2024 02:01:19 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52870118f5a2014ad2290c7f0a2f4f0d636d84e8fbd2a4e35d082411736670`  
		Last Modified: Wed, 19 Jun 2024 02:01:18 GMT  
		Size: 35.9 KB (35925 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e2a26025c773b794b1017205527019e3e364baebe4c632894d9e037477da5b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165929527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9277becade955c3951ae965f803b669da2fc9f9577f6be5f3ea1b5d4d2a79d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e339470841aa621f212ffd8e76f35790c7a28104dd97996ad2853894f3ba6`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb0cf07c9beeda8d94a25c9e65966dd25ea12f1429af47a54670924b481a81`  
		Last Modified: Sun, 02 Jun 2024 01:00:19 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54108df510677120ec7ac21fcf4d0eb9453a8dd56db90cdfd435daf38da8fb`  
		Last Modified: Sun, 02 Jun 2024 01:00:20 GMT  
		Size: 6.3 MB (6312392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e523b6e86dbd0b1cb06b5674ae8fa8aa116da11a25ecbd8dd53457590f2571a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dcf16e72cf33448e9f33b8c62b6c1552cb81a66ff80daa0eece2c353874e6a`  
		Last Modified: Sun, 02 Jun 2024 01:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1c8c168a546aca98897bb3330afc7e0075abe929da8fdd0679a7a00825c3`  
		Last Modified: Sun, 02 Jun 2024 01:00:24 GMT  
		Size: 46.1 MB (46082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326faf5381746f13b1257ec7df0b686db4d7ecdae64b4528f0ed0f79893670e6`  
		Last Modified: Sun, 02 Jun 2024 01:00:22 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91dac12e95143ff54548a09769dbfad4fb1dbd593be311bc8233dd53d8cf25c`  
		Last Modified: Sun, 02 Jun 2024 01:00:25 GMT  
		Size: 65.0 MB (64959326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2d0f6b7fbf63af609feff8e58fcc6863dab0e2a0b10a551c552a09c2b8268`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a2191007290d485ca300fc404ccfebde81da57bf9b34e901fff252f46667058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffc76a9e45ad280d89df1a984846cce67c4d845f43e22621684954575225c`

```dockerfile
```

-	Layers:
	-	`sha256:628014776a4300b4ce06f1de6c0747c20dfd212a4a63450c7658eb31eb9ca67c`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 13.6 MB (13556213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcfc2c49f5154bbd4f0595ca1b449e66ff618e6a8cae3349216d28e9c793d33`  
		Last Modified: Wed, 19 Jun 2024 01:54:53 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json
