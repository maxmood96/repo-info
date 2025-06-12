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
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
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
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42`

```console
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
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
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oraclelinux9`

```console
$ docker pull mysql@sha256:98914997054781e301d675233d76f393168ea67002424c5291072e5593350e1b
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
$ docker pull mysql@sha256:5c7658371c07e0696086f5d0c013182aa5e8de712fe45f641abf23977c15e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a378c6148ea66e1e936f825f88344307eb12962da4fcfed3252f14d884dfd`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984c0aea400a74276dffd7d2085094bf5dc1ab70a10090cd365262088e06c6e`  
		Last Modified: Thu, 12 Jun 2025 05:06:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c3e4b007a06bc8e1846094bdaf4454546fc9c9a91b2fb538e5bea5abc4ea0`  
		Last Modified: Thu, 12 Jun 2025 05:33:45 GMT  
		Size: 48.5 MB (48536415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac163d5ad357a4a0d83c8de61135d844dab775a43d104306c5fce8ab93d69e`  
		Last Modified: Thu, 12 Jun 2025 05:06:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85065940bba5ccff7bb369fbcb0a61a32fba3324b59a5185031a537f594424d1`  
		Last Modified: Thu, 12 Jun 2025 05:33:52 GMT  
		Size: 126.7 MB (126654382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce44a171d0600e7faa249dd70b918334dc908b90b9a07b542631443309c33ac`  
		Last Modified: Thu, 12 Jun 2025 05:07:02 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7266afaf33999424841e9c12f04c28ead11d83fc4b1ad6d20dea33b203e9c6`  
		Last Modified: Thu, 12 Jun 2025 05:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:259782012c95815c7a0bb81fedf839fa9f2fa0f92cc60bacedce6679559e3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e643bb5b35e110c16da2817306b031d820e4a23d781fb5a8f520ef5ca788d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ae07cf6eb77e175c5e52bfb21ae47acdd5698091174a9264922078e02a2cc56`  
		Last Modified: Thu, 12 Jun 2025 06:02:31 GMT  
		Size: 14.0 MB (14031600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add0494e7058ca59f627373455b45931266b82930ed55dde6d68fbf072364d94`  
		Last Modified: Thu, 12 Jun 2025 06:02:32 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oracle`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oraclelinux9`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oracle`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oraclelinux9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oracle`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oraclelinux9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:a458cd83af2654878d5468ff01443c8378f375b707645b597c7c75202eaad541
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
$ docker pull mysql@sha256:bc98fa85f7093af7fa3712e38ecd103912bc884945457eb13e13239b49772241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231496520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c7f45ae54b8ae571972e8e9a6d2d05b38cb008ca07ed9395637fff32b0a61`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24931c8b9941c0f9b768950ddeb3c439b29a88eaf4cc60f62aa6f5d3a64969fa`  
		Last Modified: Thu, 12 Jun 2025 05:15:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f566c2e8af01b3e4568a31a4b797a54570a529ed1f79ca54566dc6089dcbf53c`  
		Last Modified: Thu, 12 Jun 2025 05:15:14 GMT  
		Size: 46.5 MB (46515508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0421eb12ed85aaa08358adc74b79ff38f05a295ae2a7ce73776e4ac8e67de5`  
		Last Modified: Thu, 12 Jun 2025 05:15:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8fbd61a98dc8650e95c4ef6a25ac05f8bc37e706f5ff754d965bdff2e0fc1`  
		Last Modified: Thu, 12 Jun 2025 05:15:19 GMT  
		Size: 129.5 MB (129519541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf1d34195d177d1d563da13fdcb01938e62c7777db02a51d933008e2a500729`  
		Last Modified: Thu, 12 Jun 2025 04:52:40 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4cf75ed7dee905651c106d82a980846101ed506eda1314bd9c8de3b02a18b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f943ffc1ba799c39916e3b0b14e07b4c7701650a292610486dff8fa5b20428`

```dockerfile
```

-	Layers:
	-	`sha256:b7c0d1802e3e002bce2506a2e5ee3cc2db78c842023125baee5f70b5252a1e49`  
		Last Modified: Thu, 12 Jun 2025 06:02:25 GMT  
		Size: 14.3 MB (14308493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99a51effa633bf5a89b06185e30fbd4a8139a44b94d5cb7698f36df1dfa64`  
		Last Modified: Thu, 12 Jun 2025 06:02:26 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:072f96c2f1ebb13f712fd88d0ef98f2ef9a52ad4163ae67b550ed6720b6d642e
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
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
