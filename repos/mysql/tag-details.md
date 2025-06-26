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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:3a92fd416c2638a777cdd3ea4a15bd9c644657d7d702ced95c20a8074896334e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a4db7d1af29b3c65ad81751e174e49bbb1c4c7bd64a4a56eb25c785a6de7d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c80606b7abcc8baf0123f5a6ef737750f9ba3a2f297e7b664e03d62a1e38af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136f22d09a64f5f2dfaa0b135d69e766a8bae3d24e292570b54a8a82fb736c4`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e07841ef1f425472db039c61c5a02c49a94f7ada9b8de94830f07c9a89259e`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cda231802be6a42bcdcccba6ccd02c105f313005500e29dc7a02d228d8bdc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129972d409e0bdca1747a97e079c9c7461b9df4f4fdd717f469bcbd50e477fa`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a39b3bc17802ad58f6d38f3ac77a9afbddbf655652e0f1700b5f9689049cfd`  
		Last Modified: Thu, 26 Jun 2025 00:09:52 GMT  
		Size: 49.7 MB (49674947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196d276e6238c0778e1a7925a3bec11003834868927fca81cbfa905f8e3f7fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad5ccea9dc1a7227b08564a4983012886ab03fe286cf546988b9254557d1ef`  
		Last Modified: Thu, 26 Jun 2025 03:02:31 GMT  
		Size: 128.1 MB (128118721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f342254d0c4452e8fa2a50c333bc3b4cd17418dffe5e638a275946188a48365a`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d929db40fd08af565cde45deae9d91e239ee39c086486f4740386811cb9ef`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ee6d1457b67ca40d0535b64f683f35e4c27ea06833d7fe2a7984ee5a62c80d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848f8ac6ff9c7da939fe0bf85b96b86c24f062b1f9c8523be129b8d181f08e6`

```dockerfile
```

-	Layers:
	-	`sha256:359e4c93e664a398c1d0d5b2b94fb73d39afde0f2601ce35993c6adda93a0a4b`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa78c903302f24b0cb025ec48398fd9601e231d843f0a158fb23be4f4ace727`  
		Last Modified: Thu, 26 Jun 2025 03:02:26 GMT  
		Size: 35.0 KB (34952 bytes)  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:9d43fc79508d3d3341221a8ec281835f848821d596022b286474ff810974513b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e138ecfe0819b0f609f21a30ecc2a79a4a0b73e1aea5bf2f7dfca73fe91a22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d801e72dadc00d892b2d80439a66e3fb07133656e990d8828283d983e7bae59`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b61316434e9c64491beae3e617bbf77dd29dad44a8dbf644f539356d45a39`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d890323c58d057b6a047b9c7bb22ddfca1fc540e15f290b316522c131626ed6c`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fe53bcd925bf4359b69be8d7eadedfdbf9070650e6fc02b25f34be289d790`  
		Last Modified: Thu, 26 Jun 2025 00:09:49 GMT  
		Size: 6.8 MB (6814360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b4cbb089b9525736bac9e2d9b5d09d226ed9e18c8c3797ec1c544798cf962c`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb01df5266943db66313964817143d050cffdb60312874d1ebc43a9929dbf52`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c679c6396f29dbb6485a5c04ad34c6424f9e229ba62af530d7c39d71c61fa71`  
		Last Modified: Thu, 26 Jun 2025 00:09:51 GMT  
		Size: 47.6 MB (47632379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aac31a742e1a471197e224e5b971000d8c4e6a5a929e2102ed1ee48b4376ae`  
		Last Modified: Thu, 26 Jun 2025 00:09:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94fc39e14717377355db714ebd740cab885e0b58bd3cb68e9e8ca29d406fd8`  
		Last Modified: Thu, 26 Jun 2025 03:02:21 GMT  
		Size: 131.2 MB (131153119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c84c738e0aa70e716b4c12634ef2e72c1440006b6e6b282ebb1a3bc0c0569f`  
		Last Modified: Thu, 26 Jun 2025 00:09:48 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b47c0ff14b7f4a19420b4774ab5e7afc1e987163baa808aa14413bec528a6545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae773eeb1a6e3651ff2e62eafab9a97c8e82d8c1705720c004f0e58f77896a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0a60bfb4e2e5c4825a11cadc112ceb930168095f83a984c05dde90111728708`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd54d04d7dcd8f93366b25aee64143778c44157927a4a07c9e60cff22784bf40`  
		Last Modified: Thu, 26 Jun 2025 03:02:18 GMT  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
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
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
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
