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
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3350a51c92db73edbec591f738399e75ba4dd8cc05ede73597d087942f56de3`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 134.2 MB (134245460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1541cfd976704660919b071995ece082b8f6a1c8727a447bfd9cc3bd95bdf4`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dced65d3dabbaa65b13a203df29c0296e88bc1d712cde3b1415a615b02bab9`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ab40b9e6f36288846a681d00f82a18106e993b93dd5d3f0d1bcf1014ee5dd`  
		Last Modified: Tue, 13 Jan 2026 02:27:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:03:06 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:271aa4b4c84411d52790b340039dc6cea8637ab273546ff15639a77fae6b29f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:00ae178085bfcfbcab92d1cd5942da056dfb3663f212dbe99e85b156f5762958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232089764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4fad4f1f633f334629e92f6f2738d98937579e590fb39c5ea7dc0278c2535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:34:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:34:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:34:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:35:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:35:08 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:35:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:03 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:03 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310b139f7c3ac18c6a758ad8b1ade33907bfcf03b387254bac47c7d11f01edc`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fb977c6ce78c2f1c928e0140f1d4ced52ddd2f58f29694c2b5dffb4efd120`  
		Last Modified: Tue, 06 Jan 2026 18:36:42 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e746e7b2e39b437d9854022e45a1e660a7d6799f4e5a0cb71c2f9f61a04c29`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 6.2 MB (6173187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e74778c5d59e7dc79a039fd94f9c33686ae66d13ca2fbbacf42742a57ccb3`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d963f8b5a9a9ac1f77df2b14829161c399aa6fc047aa5b35aa2a4ce27d502d`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41a114e506c57e47c76dc614f9d6af75f02e005d951bc6853a4d7d8a1f354`  
		Last Modified: Tue, 06 Jan 2026 18:36:47 GMT  
		Size: 49.9 MB (49919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4bc928a8953e1da52f296d1936007ca9a37ebf5d019dab93163dec4e0af5f`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082df7bb4f0960c51ebc594096edf300e3d04e37ba1e669ea7db3c9fcdd5d7cb`  
		Last Modified: Tue, 06 Jan 2026 18:36:58 GMT  
		Size: 127.9 MB (127886619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583e052860aa1692029c708154abe757a6391984388a5938d88491423d3cfb0`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758af62b8ea8cf09257f3f49b28ea4a6cb3666bf9d5464ed3caac489f94ed0b`  
		Last Modified: Tue, 06 Jan 2026 18:36:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:254019d620010a1ddbb52d396ec1ddda17d4807abe57a7b5b14108c4d7424de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51528fae7f027181f650ed61d67ec7ec38acda3e27a3c825292717509da65dc2`

```dockerfile
```

-	Layers:
	-	`sha256:daf507697d1d368fe4509afcf217a0c3ee4c0f96e973b5b2c84646bd5fd247df`  
		Last Modified: Tue, 06 Jan 2026 19:02:40 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ee027e6dcea7efc1de2f3cd284cd42b96f6ad0f6faceb28a653fc9370feaa0`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 34.9 KB (34909 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c345a35a8c685b837d3f53edf72d05e7b199b6b0b62c038b37030b5d3c4b1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227707188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79928aad6fcff21e8a7c4c2316aaba0f33d8244fdc426f3c33a60dba7e53b89f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:35:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:35:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:36:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 06 Jan 2026 18:36:13 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:36:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 06 Jan 2026 18:37:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:37:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 06 Jan 2026 18:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:37:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:37:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90020810c99d86e2679b3060af330330a3cce5366f951929a5a47221f155038`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eece71fd1bbd5c05c9845394b0794a2cb418279073d0d9d42e85370fc8af452`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc814d60197f2ee3c4cb589f39e666ef9061e9d752bf30813744d8a75e88a55`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.8 MB (5799406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7f207950c919499c16f885bfcfa3042368d47c0a5bdb18c4c7cdedc3fc69b6`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4906835f6a1dcc63b4250598920dcfc06826d55720ee03492324549937251`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033df9eac42ccea6090d2922577b4a6edd5a7ee925e9591456a49d7449be9cc`  
		Last Modified: Tue, 06 Jan 2026 18:37:59 GMT  
		Size: 48.8 MB (48782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c69f4e227eee8147ef1bf5cf62dd4393460550c26f1f72e54c23ff37dd79d`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7085458af432660f1d1d71a7451f30aa75a1d7a866479bef2b0402501f7bc05`  
		Last Modified: Tue, 06 Jan 2026 18:38:06 GMT  
		Size: 126.5 MB (126472740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1802fdd3c4faaa05becc6253c8ee5be4f689457c6003a3141a9daacff7e6bd`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc5248e917ef56803fd734711bf7b96091544ed2bd66e6f1ded89b08847921`  
		Last Modified: Tue, 06 Jan 2026 18:37:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6e6cbd181b9e398a6e02c0513a9f73f34e1b92e46a1c28f6b21372c503a567d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1024e898dce66b7dd6282e02713603174626219fa62bf7cccb6ca729bf8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:d7eb966ee32882bbd7b4aa000af8f566688ee3a27c037d9936ac16a70917d5cd`  
		Last Modified: Tue, 06 Jan 2026 19:02:49 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa929058e4d718a761246a7e16e219ab3bbcee3d44ebf0753e9263757ab75dcb`  
		Last Modified: Tue, 06 Jan 2026 19:02:41 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:90544b3775490579867a30988d48f0215fc3b88d78d8d62b2c0d96ee9226a2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:615302383ec847282233669b4c18396aa075b1279ff7729af0dcd99784361659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233028429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c6e074ef93c709bfd8e76a38f54a65e9b5a38d25c9cf82e2633a21f89cd009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:34:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:35:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:35:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb2baa39f3c794a800ae1bc1d6ca7f4af9f2c32b4b01f3b36b0adf94acdee7`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d96bdd8a5024d9e98f2e262976e0b0fc3aaba0dee458e17d3a65ffbf1dc327`  
		Last Modified: Tue, 06 Jan 2026 18:36:14 GMT  
		Size: 47.8 MB (47809903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ab04cc1e9ad55eec420f0c1bb00f0138aa7d8b4e1808845a06f0a1f523a6a`  
		Last Modified: Tue, 06 Jan 2026 18:36:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4df3fa85f6f1e04893ba769aae7460ef477938531e57a689d520fff915b2d`  
		Last Modified: Tue, 06 Jan 2026 18:36:33 GMT  
		Size: 130.9 MB (130935386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32caf90444d407306899d885aee85a926027bf92d943a67a128da4d3c2dfec`  
		Last Modified: Tue, 06 Jan 2026 18:36:11 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c1f109b1be92ccf9544297c60085d8962f088d159263d68ecc1c0328e3d5beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997be7b27df029ec920fcb9ba53acbd1867100528b4ef1d822e9fde8c7550b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4591f84b2535834017f2f74b1aeb64b2f419b2d75aae8edff3f4d65cb4e60427`  
		Last Modified: Tue, 06 Jan 2026 19:02:25 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083d2b6811dd8c9aa22da74afe55b797b5bf8254cdde3418cea3be32f70aa66`  
		Last Modified: Tue, 06 Jan 2026 19:02:26 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8dda11a181d09656bf71c7cb841e76adb5b673d4f91c33268651a6ccca6c932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228473394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b86b5c8b031c53b86d61c450837fa1b0d2e48d839e196d788915bf7c2a4a72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:35:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:36:02 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 06 Jan 2026 18:36:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:36:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:36:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b50e039b7be821f64d9203438b377b5f23b473fe523061a1974e1806b4b028`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e517690c80a7a5a11740ff6d12e9f334e77d241574c5b6260a53a3d68cca8`  
		Last Modified: Tue, 06 Jan 2026 18:37:24 GMT  
		Size: 46.7 MB (46688745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500efaeeb4f1d7d45f0c8726e8f83e203a1752f7aaa57eab0ed8dc5d764d0cf5`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb188be37b083448c633d6e952c62b1d51cf0f6ce818bcedb617bf94e98b13`  
		Last Modified: Tue, 06 Jan 2026 18:39:25 GMT  
		Size: 129.3 MB (129332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b701d63240c2a319f3dcf1d7224b8c3e8b081291acfa8bbd421abd4155fe1`  
		Last Modified: Tue, 06 Jan 2026 18:37:19 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50bdd6c2a5e98f5d7bc1f4885ee7f4f05cdb68b81940266e58b036344b668185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6a6ce5a6df253205ea157731114b52bc1b9c6005e8abc196c4e10c8512db2`

```dockerfile
```

-	Layers:
	-	`sha256:a867ed86977ef24a92d0adecd6bcb3630df611260827b30512329f461ba55cad`  
		Last Modified: Tue, 06 Jan 2026 19:02:36 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a02a3c5afb7ba7440136999f1aa866a69b5076cd20cf2a2dc18ef73d14f080`  
		Last Modified: Tue, 06 Jan 2026 19:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
