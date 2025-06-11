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
-	[`mysql:8.0.42`](#mysql8042)
-	[`mysql:8.0.42-bookworm`](#mysql8042-bookworm)
-	[`mysql:8.0.42-debian`](#mysql8042-debian)
-	[`mysql:8.0.42-oracle`](#mysql8042-oracle)
-	[`mysql:8.0.42-oraclelinux9`](#mysql8042-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.5`](#mysql845)
-	[`mysql:8.4.5-oracle`](#mysql845-oracle)
-	[`mysql:8.4.5-oraclelinux9`](#mysql845-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.3`](#mysql93)
-	[`mysql:9.3-oracle`](#mysql93-oracle)
-	[`mysql:9.3-oraclelinux9`](#mysql93-oraclelinux9)
-	[`mysql:9.3.0`](#mysql930)
-	[`mysql:9.3.0-oracle`](#mysql930-oracle)
-	[`mysql:9.3.0-oraclelinux9`](#mysql930-oraclelinux9)
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
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:7345e765cf5fa9359b62f0120fb364cf942254a4a09617487c60341bb853e5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:79e2b6f30312219ce566d3bcea70ce06cf27e2062d4cebd4a9cec89c7f044fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183351637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de05dd69bd899838c8b4e62ce7e92d76e3aeb8830827e13798e5629ec249dec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63bb4405ed73ed3a72dca4226494112793f62408148ceb7d110735023457e73`  
		Last Modified: Tue, 10 Jun 2025 23:39:19 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b6356200dbd167977462098bfd29e82b0afea13d9e146e360777db7f7f6586`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d155da284d9189cf7b1482661ab05819891364f1ac14e221cd16bdbffd4421f6`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e66f6d6f872ea7b3a5e7da802089a1ad76e5ebdcc69ce6965cf6321652f11`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e7237a6e3cb1ac3bd7b4b279f1459952b33fad68af388a041a5648b4b0443`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 15.3 MB (15295813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d3ee2fb6b578ae153abba07d54ace1898b594e7c62072b334ef6545557cc1`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d421a53d79e35ed51dad927dbe8d36d87a097a5f1f0697cca876bea208435a8`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd426f717bf76f20ee8e64f46fcc92eca9650fd01829ac94d43e2edb646d16df`  
		Last Modified: Wed, 11 Jun 2025 03:02:42 GMT  
		Size: 133.9 MB (133946677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca754f7f8d7f008240038760e775aa8aabbaaf604999aef11a51fc2e70a7b6`  
		Last Modified: Tue, 10 Jun 2025 23:47:04 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2675006f648bd43f41a991326a6a465591b9ff581cda967fd7d6035ab6e694b`  
		Last Modified: Tue, 10 Jun 2025 23:47:06 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628abadae87a555c23aba9bb398ab143ed1e0ae4824964a2a37b07601c4fd8f`  
		Last Modified: Tue, 10 Jun 2025 23:47:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:7cda1ab139407fd89118a2e18a8ee849b1b3590f6b78ad533c173087bf63d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802ea45d0cdfc89f565e590b8dd1e7ff276d563d3d86b14ff635fc4d2e48160`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c3eb4f70c97aaf4a3b5174db449aedcaa445877e978cb26f0c5ea6093e09`  
		Last Modified: Wed, 11 Jun 2025 03:02:20 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b256699448cd6532562bbef884b57949e6b2977c4f924f2cf3b6e3ee642a6d5`  
		Last Modified: Wed, 11 Jun 2025 03:02:21 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:7345e765cf5fa9359b62f0120fb364cf942254a4a09617487c60341bb853e5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:79e2b6f30312219ce566d3bcea70ce06cf27e2062d4cebd4a9cec89c7f044fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183351637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de05dd69bd899838c8b4e62ce7e92d76e3aeb8830827e13798e5629ec249dec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63bb4405ed73ed3a72dca4226494112793f62408148ceb7d110735023457e73`  
		Last Modified: Tue, 10 Jun 2025 23:39:19 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b6356200dbd167977462098bfd29e82b0afea13d9e146e360777db7f7f6586`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d155da284d9189cf7b1482661ab05819891364f1ac14e221cd16bdbffd4421f6`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e66f6d6f872ea7b3a5e7da802089a1ad76e5ebdcc69ce6965cf6321652f11`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e7237a6e3cb1ac3bd7b4b279f1459952b33fad68af388a041a5648b4b0443`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 15.3 MB (15295813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d3ee2fb6b578ae153abba07d54ace1898b594e7c62072b334ef6545557cc1`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d421a53d79e35ed51dad927dbe8d36d87a097a5f1f0697cca876bea208435a8`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd426f717bf76f20ee8e64f46fcc92eca9650fd01829ac94d43e2edb646d16df`  
		Last Modified: Wed, 11 Jun 2025 03:02:42 GMT  
		Size: 133.9 MB (133946677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca754f7f8d7f008240038760e775aa8aabbaaf604999aef11a51fc2e70a7b6`  
		Last Modified: Tue, 10 Jun 2025 23:47:04 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2675006f648bd43f41a991326a6a465591b9ff581cda967fd7d6035ab6e694b`  
		Last Modified: Tue, 10 Jun 2025 23:47:06 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628abadae87a555c23aba9bb398ab143ed1e0ae4824964a2a37b07601c4fd8f`  
		Last Modified: Tue, 10 Jun 2025 23:47:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:7cda1ab139407fd89118a2e18a8ee849b1b3590f6b78ad533c173087bf63d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802ea45d0cdfc89f565e590b8dd1e7ff276d563d3d86b14ff635fc4d2e48160`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c3eb4f70c97aaf4a3b5174db449aedcaa445877e978cb26f0c5ea6093e09`  
		Last Modified: Wed, 11 Jun 2025 03:02:20 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b256699448cd6532562bbef884b57949e6b2977c4f924f2cf3b6e3ee642a6d5`  
		Last Modified: Wed, 11 Jun 2025 03:02:21 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-bookworm`

```console
$ docker pull mysql@sha256:7345e765cf5fa9359b62f0120fb364cf942254a4a09617487c60341bb853e5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:79e2b6f30312219ce566d3bcea70ce06cf27e2062d4cebd4a9cec89c7f044fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183351637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de05dd69bd899838c8b4e62ce7e92d76e3aeb8830827e13798e5629ec249dec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63bb4405ed73ed3a72dca4226494112793f62408148ceb7d110735023457e73`  
		Last Modified: Tue, 10 Jun 2025 23:39:19 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b6356200dbd167977462098bfd29e82b0afea13d9e146e360777db7f7f6586`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d155da284d9189cf7b1482661ab05819891364f1ac14e221cd16bdbffd4421f6`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e66f6d6f872ea7b3a5e7da802089a1ad76e5ebdcc69ce6965cf6321652f11`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e7237a6e3cb1ac3bd7b4b279f1459952b33fad68af388a041a5648b4b0443`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 15.3 MB (15295813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d3ee2fb6b578ae153abba07d54ace1898b594e7c62072b334ef6545557cc1`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d421a53d79e35ed51dad927dbe8d36d87a097a5f1f0697cca876bea208435a8`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd426f717bf76f20ee8e64f46fcc92eca9650fd01829ac94d43e2edb646d16df`  
		Last Modified: Wed, 11 Jun 2025 03:02:42 GMT  
		Size: 133.9 MB (133946677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca754f7f8d7f008240038760e775aa8aabbaaf604999aef11a51fc2e70a7b6`  
		Last Modified: Tue, 10 Jun 2025 23:47:04 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2675006f648bd43f41a991326a6a465591b9ff581cda967fd7d6035ab6e694b`  
		Last Modified: Tue, 10 Jun 2025 23:47:06 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628abadae87a555c23aba9bb398ab143ed1e0ae4824964a2a37b07601c4fd8f`  
		Last Modified: Tue, 10 Jun 2025 23:47:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:7cda1ab139407fd89118a2e18a8ee849b1b3590f6b78ad533c173087bf63d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802ea45d0cdfc89f565e590b8dd1e7ff276d563d3d86b14ff635fc4d2e48160`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c3eb4f70c97aaf4a3b5174db449aedcaa445877e978cb26f0c5ea6093e09`  
		Last Modified: Wed, 11 Jun 2025 03:02:20 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b256699448cd6532562bbef884b57949e6b2977c4f924f2cf3b6e3ee642a6d5`  
		Last Modified: Wed, 11 Jun 2025 03:02:21 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-debian`

```console
$ docker pull mysql@sha256:7345e765cf5fa9359b62f0120fb364cf942254a4a09617487c60341bb853e5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-debian` - linux; amd64

```console
$ docker pull mysql@sha256:79e2b6f30312219ce566d3bcea70ce06cf27e2062d4cebd4a9cec89c7f044fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183351637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de05dd69bd899838c8b4e62ce7e92d76e3aeb8830827e13798e5629ec249dec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63bb4405ed73ed3a72dca4226494112793f62408148ceb7d110735023457e73`  
		Last Modified: Tue, 10 Jun 2025 23:39:19 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b6356200dbd167977462098bfd29e82b0afea13d9e146e360777db7f7f6586`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d155da284d9189cf7b1482661ab05819891364f1ac14e221cd16bdbffd4421f6`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e66f6d6f872ea7b3a5e7da802089a1ad76e5ebdcc69ce6965cf6321652f11`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e7237a6e3cb1ac3bd7b4b279f1459952b33fad68af388a041a5648b4b0443`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 15.3 MB (15295813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d3ee2fb6b578ae153abba07d54ace1898b594e7c62072b334ef6545557cc1`  
		Last Modified: Tue, 10 Jun 2025 23:39:20 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d421a53d79e35ed51dad927dbe8d36d87a097a5f1f0697cca876bea208435a8`  
		Last Modified: Tue, 10 Jun 2025 23:39:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd426f717bf76f20ee8e64f46fcc92eca9650fd01829ac94d43e2edb646d16df`  
		Last Modified: Wed, 11 Jun 2025 03:02:42 GMT  
		Size: 133.9 MB (133946677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca754f7f8d7f008240038760e775aa8aabbaaf604999aef11a51fc2e70a7b6`  
		Last Modified: Tue, 10 Jun 2025 23:47:04 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2675006f648bd43f41a991326a6a465591b9ff581cda967fd7d6035ab6e694b`  
		Last Modified: Tue, 10 Jun 2025 23:47:06 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628abadae87a555c23aba9bb398ab143ed1e0ae4824964a2a37b07601c4fd8f`  
		Last Modified: Tue, 10 Jun 2025 23:47:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:7cda1ab139407fd89118a2e18a8ee849b1b3590f6b78ad533c173087bf63d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802ea45d0cdfc89f565e590b8dd1e7ff276d563d3d86b14ff635fc4d2e48160`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c3eb4f70c97aaf4a3b5174db449aedcaa445877e978cb26f0c5ea6093e09`  
		Last Modified: Wed, 11 Jun 2025 03:02:20 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b256699448cd6532562bbef884b57949e6b2977c4f924f2cf3b6e3ee642a6d5`  
		Last Modified: Wed, 11 Jun 2025 03:02:21 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oracle`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oraclelinux9`

```console
$ docker pull mysql@sha256:27dbc615430671ce580ddc5b2d816c19e695c0300437480cbe547e6e317d752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:74f1196bf779e1f9bb08e00208d4e3c54db03ddcc9a0295b4c645ca209f70fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235094324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355bbda86f666a7cb3e0030cdf6ebfd97af2eb3112b7338341dd5768139ebd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328331c039e1a49160b8fb1496c2243e682eec31ae9858317a7e7fa8116687bf`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d496fd643f61cc7e94438fe9a959dd6300e23bbe8f87325533565ada7729f`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd3c96f0d10d2d5bc09a2b9c83db277c77f367bef3e1076a187ca2a29a9741`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20801d69c6c33a37d96d1cc9fb551787233e68c8d57593591adc1dd936d85300`  
		Last Modified: Wed, 11 Jun 2025 17:34:44 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadb37d0131835e32264ec5ed317908a8cffdb49478595d64b7ea30e6fc747d`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5a4e5a73b089e4e55e8b99e50adc5acee5b9c8ef40deb729bfcc340ae9853`  
		Last Modified: Wed, 11 Jun 2025 17:34:49 GMT  
		Size: 49.7 MB (49674091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e3ece17cac78c47a69c769629efe12071c10b7f9e55ec7e88e352302446e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514ed45da954b93e63fb34076057874ff82a5a64f8b4ee4a33428be57edf121`  
		Last Modified: Wed, 11 Jun 2025 18:02:38 GMT  
		Size: 128.1 MB (128110376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204a3e55e5c579a6cf61dd8a5bfd4921afcdc0e7d3a1c9553655fe989de501a`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4d41f857fef3801a10f4b7fbe9a0379300da132c259bb9ae2d6f369dc8a6`  
		Last Modified: Wed, 11 Jun 2025 17:34:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f6aa553560de6a7ff88d95b70f58d58b4852ed5243fd74fa8cea970ff67740b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf65a02198e450ff0501e0b7e324f8e93c80dbfe57a7d7c010fc834913ff03`

```dockerfile
```

-	Layers:
	-	`sha256:c516089d662b40bcc1b0c7a1fc4c07d70a35bbf86c918ce880caeb8ffb82fb30`  
		Last Modified: Wed, 11 Jun 2025 18:02:32 GMT  
		Size: 14.0 MB (14033253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bfe4f17acb0e0a191d2daf6cd3ecc7fae450d58176075cdece69e92ffd9a3a`  
		Last Modified: Wed, 11 Jun 2025 18:02:33 GMT  
		Size: 35.0 KB (34953 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edcba760ed028a76d4cdec6d2fcc768a0f03c528ba3aab11894bc5bd3b1a1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68693e8f4b69a52343607ca444802d54a78554e3e68a8d0cc30acbcc7359b009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1a27fddd7477a8dbace90f0900e58ab0663350d533636a42ff6ee7723c2a5`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff1a7d0b95713cbaf565a0d457b7a3cfee15abe95260e1a1da823ef8bd8bed`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 48.5 MB (48539444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916821cb1078c32bfb22384c771018283284e7b7735a178f2d66d49d7e0080bc`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441bab40b11b2c6555e27589e9498851a2e0dce6a6a88166b764ca45b97cdf5`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 126.7 MB (126651226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81166cc94f64b8d17661bb7ce2bf93232ee0855f530e2867ec2a33d5616ea948`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6025c601726be40ad6f85a9ad15828a81cf21f66fe4c75b7c9dd5e857efa6`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5205649dc1636bc82be0b5613fb1ffe596d3e0b2850ee95a15ab73c19c62e7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35747e0cae6060a9767216dc350b5f6b000e1d650d707add4f7b980b456c5f1c`

```dockerfile
```

-	Layers:
	-	`sha256:bc070b57b7e8dd80222cd784357d6ae964e23e011709cc7d300640841dec3a44`  
		Last Modified: Tue, 03 Jun 2025 15:31:02 GMT  
		Size: 14.0 MB (14037283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc18603f28aba0d299df567443de2be7c99f28ace167bb49c865723b00f9076d`  
		Last Modified: Tue, 03 Jun 2025 15:31:28 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oracle`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oraclelinux9`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oracle`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oraclelinux9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oracle`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oraclelinux9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:ca48cb49cefd64b6fd062c38719061922c2f79332669d9b86f91480b982778ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:067f8ebfd40deaeafd704e19866800a0a7c0fab921fcc231063e371656e2860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbbf951246a9ed3bc6bf53df5fbb2c4d07753f9e10af237c03a2aaf56653ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6917113d1d32bb7ec391b2ed1f20cbfd60fc800022750bb6ad78ee67375b`  
		Last Modified: Wed, 11 Jun 2025 17:35:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b01bf9502d63cc031edb8a19ffbe7dc551782c7e733b77855a941f75486c86`  
		Last Modified: Wed, 11 Jun 2025 17:35:03 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304994821db8362337069dce4e8c238a82a765f94f04a4ae6129b3300572ca0`  
		Last Modified: Wed, 11 Jun 2025 17:35:09 GMT  
		Size: 6.8 MB (6816291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f1b9314e3e30dd8e7d954bec1d256f24d9a96f6beb66a532857d9f40933c1`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58722f6ab2ab82d1e3fc42778c6cbc7f2a4a11c1d50f0635f2f774496b4659`  
		Last Modified: Wed, 11 Jun 2025 17:35:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18956553208fc086aa2ff968f6ee769aaf9d25b02f68b31ee08d5132020d70cb`  
		Last Modified: Wed, 11 Jun 2025 17:35:17 GMT  
		Size: 47.6 MB (47631196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3202a60023ba30e7fa5903c45f320f685692ba62b8bea2fc941a58109114c`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3b77cdda9cafeea121f7385b3c525d379d31ed665dc4ddd2e000c8cd6aeb`  
		Last Modified: Wed, 11 Jun 2025 18:02:29 GMT  
		Size: 131.2 MB (131154276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d9caf79fefb6b51d5107c65267b847b0458ee7bfbd2ff59172d7146f21ed8`  
		Last Modified: Wed, 11 Jun 2025 17:35:10 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6b30302cb94e9de3855962201afd58ab9b8690ac06a10abb5c46261b7bc1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c20d1519b167c4bc91f63d81e2faa9df39342feba7ddd963f6411e72a53c1`

```dockerfile
```

-	Layers:
	-	`sha256:7d20e0288de24c69299c9af3458dc4a4b1a454431c1d79a86e843bf87cebab3c`  
		Last Modified: Wed, 11 Jun 2025 18:02:27 GMT  
		Size: 14.3 MB (14310074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e08692f7ee7548f3463d3a601d9aa2c1079ec6430b96c13f15d712cfc13ab`  
		Last Modified: Wed, 11 Jun 2025 18:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1af6659b53d64d9e8b6ddcd743675768d306ff8c02f51efb177ba752c732c8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9e58977a4db7b5397af1d54535e1efdff8b0ad320b3ffb01a8327d2465544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20409e1dff4e65ef9bde52df41d8aeb392395d44ec89fa0d075868a668b2f905`  
		Last Modified: Tue, 03 Jun 2025 13:31:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a2a20b561e8b1a7ae71e2f7dd2aab8470b5669f7645130ca206bbbb8f7832`  
		Last Modified: Tue, 03 Jun 2025 13:31:37 GMT  
		Size: 46.5 MB (46518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51591309b76bc8ffbe16c2b477ab64496652549955341adf3b5204ebe61eb60e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe34e10dee2a8cde9bcc8a78a161ae7ec4833752ec9eea3ddbeadcc81babf9`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 129.5 MB (129520471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f123a98463c2a3ad6cdc9445af1478b83853a2deafaeba9b06b05e2a177d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:70682133c7df5fd28cb00224bedae27f2b8b548819fde9beabe4d6d2b148a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14348732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e105406efb18590969ddb85c039d200714b012b43759eeae2500352e8c6b77`

```dockerfile
```

-	Layers:
	-	`sha256:5ec8be5dde16a1a4e787a7e9f1c3537e7d3a82c6e1d6e5ebc96272420f0c2a47`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 14.3 MB (14314176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c65d3c031b52712b72e8dc3d0038e2ccad81a2231673d713998fd2155ba9718`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:b3b4f16bc88942b35c6e4550d38dab99bec82ad3bef9340131155673f40a1b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6432d412b5f7132d4a5a4a1cf5d7cba9aa4cbe0ae4da5e11ab37c65fbe5ae702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258103296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af67d37072da6db21cf28ad7413ea19e6ed01ea78e839d7364641518d4eb863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86362e2a75e4fa8e4fd776f58ef42ec8a5ba9e4b4231879a476d65a3110aa048`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155de89fc7360fd0a2994207de7d491d3c32b9aa1664a2879d81df2043faa6`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770ba94c1033036d296d79303b3e6491c0a2ee4a8303f89a746b9956f6f1c1e`  
		Last Modified: Wed, 11 Jun 2025 17:34:45 GMT  
		Size: 6.8 MB (6816455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ba43c350ceb698b22058ff9b9d9b4a82b6db8b8deab584deb42e5a5c7c559`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4efd3f008b72aaafabd68531e96ad327756783c3717c42f2636042a4c9079`  
		Last Modified: Wed, 11 Jun 2025 17:34:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b97b02f10edb5b9844d1b4c022f7ff49ba347dbb2e423ed10f9cc7091e0294`  
		Last Modified: Wed, 11 Jun 2025 17:34:52 GMT  
		Size: 48.4 MB (48429791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44111e3dd4e97e794f8bcf7a13a685b4ca06a8bfddee61755eadf120fe7af4`  
		Last Modified: Wed, 11 Jun 2025 18:01:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2bff0604d581f8ef1bfbde606523cbfdca2d71d99cc4287fa95780f167cf`  
		Last Modified: Wed, 11 Jun 2025 18:01:33 GMT  
		Size: 152.4 MB (152363664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d7f5cf2247256e3335f3c36e095a249013f9e8421bd2c2d67d71a9eab4387`  
		Last Modified: Wed, 11 Jun 2025 18:01:20 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44b78be9b3d718088b3531147feeb91c0ff88edfb373dd02bbd1d204fcaaefba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf6f5fea8a25d5ed8fb000c35eab40e86b63fec4a7062798ca840f800aa366`

```dockerfile
```

-	Layers:
	-	`sha256:f82a3ac86d3e28345412abe62e975050fcc6479d60303c04c215539b71ed8cd7`  
		Last Modified: Wed, 11 Jun 2025 18:02:45 GMT  
		Size: 15.1 MB (15076572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66816b2acff78613b4dc887df3cfff6690cf4d5a1c12b1d50e8a110fc1b4a8`  
		Last Modified: Wed, 11 Jun 2025 18:02:46 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f8e22f917e900191fe1eadf8bfc6e6ab2421fbf790f50c55c983ad1fa47cab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253378207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077644601b9ffe0a3010f11dd3f6f5e4f027e32cf8defccda702411504e74e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60700820da4176cf53a62caa9391137a613935d2ceec3da86592b1643d2054d`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab094bee8180b173902cba35bbe9299901c3e7eeda52c84c4c9789f13e80476a`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dde699bad4de6297a41e73624fbbe0de6ad454c9128be07a5c3a2549c9358d3`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 6.4 MB (6449725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f3f511931aab49333a5f749ba93848404d1b7e8be495603ba40e1b0d15ca2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25b4731a5f1af97eb1c4b8b8763f589f8de8ffeef0b8e5f8b77522454df2e0`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001a86ccdd648ec9095cf4ea6b9fab853603eadf58fe7a4b6e759bd4a28a026`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 47.3 MB (47276413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeda1adde2068a5c8c9154bcfafc280d0b3ce546ea46d3ac8b678104b6070a`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeadf9132da468a5c889e1971a39df6101306678c7620ea9f68df891ece241`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 150.6 MB (150638561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14ed418aac72ac319513a92cea496670cde7161b691548a7b8550b390d80b5`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bbf39782b5484707b78ee01e80c9bcadf49a9c37e06aaaccb1e37eb18ba23fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15116369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bdd0ed9157a60e3d6cf79f2f5f3b4b2050657f44150e791dcab79793ac0eeb`

```dockerfile
```

-	Layers:
	-	`sha256:6ebc3628d926a81de427c6ecfad94bec19918e568ac0a89efbe27d7c1c111b60`  
		Last Modified: Tue, 03 Jun 2025 19:51:49 GMT  
		Size: 15.1 MB (15080710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6efda7318c21dc7b346509371fbfd673f835c6b04e2f9bc5fac3ddabdceaa6`  
		Last Modified: Tue, 03 Jun 2025 19:51:46 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
