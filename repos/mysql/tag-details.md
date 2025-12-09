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
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-debian` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:0275a35e79c60caae68fac520602d9f6897feb9b0941a1471196b1a01760e581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:767f788cdf72a451551137170a10e8b9d1dccd3316c67b490e8534d2fa94a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232090528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f1309164f3465ca13aa0094587ee7322877800e801bb8430ac599ed803fb63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:15 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c731ffd1a30b5245959c750687301950c6d3f5fe82f86fdd028bd48974a77a`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c09a342d40c936031c632d5c7f1173bc6d90bb85572af698fdc19ef3050107`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8812fa3131005cb845fa227aa443d8054629dafab384eca5760f8b2cff06ac`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 6.2 MB (6174364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96682d77f5a0d4ce6e985c25472d45ba812be2dc13ab883d9dec1ec3d25f1ba9`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ef7d4d76b32be3c2410741d0afef8afc20894deae5220e32a751fa985e89c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7bd505eaa0c311badc4718fda81b05d5a822fd59c42c31e5c4d43ac31cdb58`  
		Last Modified: Tue, 02 Dec 2025 21:32:00 GMT  
		Size: 49.9 MB (49917893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907afe780e24474b1a0f32ee47cae121fd41884f0b65e888007f451eef97e13c`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3cd0b3401c140343345560e42050c38101b35ba93263ac95b2002d2b084dad`  
		Last Modified: Tue, 02 Dec 2025 21:32:13 GMT  
		Size: 127.9 MB (127890374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f838d3bc36392210f5b67de39ff69f6b550fd697923cd3206c09735c52986d2`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddab5f772d85e9500eec5c53d24fc28ed67e4ff7581e33c73247bc222d439f8`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e8c7d0edbc1b652709acdb62bc73a6235fed30403a12205cb139ba8851f0ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5628958b9251db815d2d6123a4c5b287456710af8e723901809f963cd0327d92`

```dockerfile
```

-	Layers:
	-	`sha256:aee39e6a64d8edfd231cc88cde63d135a53894a459310dd0d254d3ba64870add`  
		Last Modified: Wed, 03 Dec 2025 01:02:34 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15afd3a0ae59fbd6185460eb68ec80e04f9aa12dc3800c70912ceede68f8d00a`  
		Last Modified: Wed, 03 Dec 2025 01:02:32 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:69619bb30f0184c6771087ec6fd151a6bad3909d646b4314511ce9fd256ff761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227696008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98686c601ff25d0b670aa58e87479a480765aa5b08f535a47ddb323fd69f2d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:30:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 21:30:39 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:30:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 21:31:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 21:31:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fcb5fe6b80920c4544b980d684c9994037df19ceb57e17ab6acf437c89375`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e98e12049ffd619646750f0ee0a7ea8a87dad956682b8663b3e8d5d26339e5`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefaae1aee172a18d569df1bd92a341db7311af006d211c9bcb3d02aa437d1c`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 5.8 MB (5800505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad029ad6b3fd31cc78fac583ac3cd15c418b83a16079031778175846f063f`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fb5942a4db7d5158897ee2a1866cc9a45b059c644e1a50056eeff53406a3`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8b580cccd5ce36cee26708178b18e8557baf1bccfb25a7ab356fdbee3693a`  
		Last Modified: Tue, 02 Dec 2025 21:32:27 GMT  
		Size: 48.8 MB (48782674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a702cd080e39fe663937ffc77ec5efe30b211b98489c5615ff5fad5238c037`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ec3e9c020b34b0c7b6ea3f56fe1a4f3d4ca4d01b3ca34bc6230436eef3ccc`  
		Last Modified: Tue, 02 Dec 2025 21:32:40 GMT  
		Size: 126.5 MB (126468680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c45335a3bb3c0a108981e52efe827a4855b2ab79752e8d424c095962c65830`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44803d6a5f0665aee65c36c24616a3a3988875c4e33d8c194a947d2d01bbfc75`  
		Last Modified: Tue, 02 Dec 2025 21:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:175ee8622fe50c3c08ba1d5f084fa8a87a6b8e1fdb636b685c0fa743bf37d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007b69aba3d8a74a9991ef348a05c1bba88b947c1c6ddec993b4e1a6bf6da3f`

```dockerfile
```

-	Layers:
	-	`sha256:ce3c7065b96591be5e1eaa1d1ca4fe27413f8a73b86115c1c0f42e9b4f6d2a0a`  
		Last Modified: Wed, 03 Dec 2025 01:02:47 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f424b1298731f420575a324789b9e57e25f75199ba8605a0c088f962c4fb5093`  
		Last Modified: Wed, 03 Dec 2025 01:02:48 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:5cdee9be17b6b7c804980be29d1bb0ba1536c7afaaed679fe0c1578ea0e3c233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2cd5820b9add3517ca088e314ca9e9c4f5e60fd6de7c14ea0a2b8a0523b2e036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233018774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0be4ee45242864913b12e7dc544f29f94117c9846c6a6b73d416670d42438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:12 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c71e5d2da59ccb38d3b7e184ee2e4a8c6f4ae87b963743aade87efd93c53c2`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c57ddb1a7e44fce1fc349599c6b523945d225971d26c7ac084bd2e568ceb7`  
		Last Modified: Tue, 02 Dec 2025 21:31:47 GMT  
		Size: 6.2 MB (6174314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff14fd324e3f04aee3b838d4940a76d2a71b939bb97cd6dc372d66577a2783`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ca20366ccfeeb37bf85b3f62c88018d5345a7c14bec4aa76b5d06f5e696c1`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5342c4477b01d4b912c7e20283acf587fbee1537019447b227b3049e28cea`  
		Last Modified: Tue, 02 Dec 2025 21:31:53 GMT  
		Size: 47.8 MB (47809825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b65e61bf70d6b8418d8e7e8041e2f434ee20e2f77a69bbf58e306aa057d8af`  
		Last Modified: Tue, 02 Dec 2025 21:31:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f31baa56adfb3b4c28c3d6b917e7ee5906cd534ba56b7ba6d5e94d7823129`  
		Last Modified: Wed, 03 Dec 2025 01:00:19 GMT  
		Size: 130.9 MB (130926868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37513b3845df3fb755d0d340f3e90212ba0bdc1943830b2c10dde8dcd89b`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:95fe44c7f254b03e42fc3518df0f636f931b2b7be35e58c338cfef63415aaa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3a33f07bf89ef8e663789be7e75e8835104745761d867a974e1b918173d1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c3b4f448bb9584c3eea93b84d18b2c60377ef4038e0955ac6144218e41f09976`  
		Last Modified: Wed, 03 Dec 2025 01:02:23 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de2fc0b43d21549da34321b9a178c33fd8fac553425406360ce69eea448301`  
		Last Modified: Wed, 03 Dec 2025 01:02:24 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f786525619c291800ac62b843d276de84dae6a6f7c6a1fc62193c080ca2b77bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228465723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4998de4c036986f7cdfe080a1f79b1b3278301e02e7de8a40d3d9b978c18d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 21:30:04 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:30:04 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 21:31:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b7f9671cf3b8e55608e806a1342c081b309c402450c4f6a6c10dfc13e1ec2`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6a6d1ef4de7b98eacbb765e48b6478c6ad268d405e7077768ba1282c1547f`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a1db644afa6336acb445adefa65b56a91fce249b7bb717302bbabb38ce033`  
		Last Modified: Tue, 02 Dec 2025 21:31:57 GMT  
		Size: 5.8 MB (5800481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ad627b62ff8e4951e67adf94e688279f189f752f00259ec38b273d8978762`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c51ebf948dc22d3e95942cf505fe5b217259dd33707072c70a2e98af2fd8aa`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2d3ceaaddb279461da38604b392becd143b37ac2557faf7c2800a6b583896`  
		Last Modified: Tue, 02 Dec 2025 21:31:59 GMT  
		Size: 46.7 MB (46691741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4cfb5fe2068a8968fe127ce2b91599f83fd09fb2ae6d7e34e93e0f6424bb4`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74244108e2a283983a7cdaf1d943dfe235313c21096db61d8420b0e2bae6a5c2`  
		Last Modified: Tue, 02 Dec 2025 22:45:31 GMT  
		Size: 129.3 MB (129329466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536cc648f7f49be82837afa7691ec4bf496e99d4f092e4d29510a6e73eae1b01`  
		Last Modified: Tue, 02 Dec 2025 21:31:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f0785672d9994de850906e6ed7e66c13389b92314eaaabfb86177e6d447a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd8467d7194eb6af4fa99a085b0d1bb8cb7bd1569f099ff43b85b62ad4b394`

```dockerfile
```

-	Layers:
	-	`sha256:f98c3c99e2c108bfcde4d1de93b018e5734f10534bfd2d9e4795ad852b3c0e78`  
		Last Modified: Wed, 03 Dec 2025 01:02:36 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f83fa36aff7cee06a5fc67fb4bbddcb7c78451385a781b556aae94df310a7fb`  
		Last Modified: Wed, 03 Dec 2025 01:02:37 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:fe036967257bf11aab7184e371920c5b629f0dd36cbefdf4ccd2ae18cc900dbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6c859f5932ce6ea4650934178e45aa487b2d4843e25c7615102254c16c448ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274742748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3a44f3de19b6af2b8bc4353531940d525d873bc7bf224aaaa69546cb2351c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:11 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:11 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:35 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843491434c1b07c31748adf3b842ab62df7add71080237d41211bf34f0d6d06`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd38a2d7408c8f5a12a64abaa3718df12afeac77a9c49b9db32b36d6532c27`  
		Last Modified: Tue, 02 Dec 2025 21:31:46 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f85a7d691e40e69b0013ecf1b9cfafb7d6b2dec47d83cd3c5ac60b04df4b3f`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 6.2 MB (6174330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f376e797b15a1370f36cf1eb04dcc6329fa5da014a13180737fa4ee74fa62c`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a3aa7003a7ca34d110a115d205314f386b8aa3e8e8aebc0cb854d5af94cfe`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff72f8f4e985061b997ef9c294035c2bf1ec802562f9b61214612e7b02cd6b8`  
		Last Modified: Wed, 03 Dec 2025 00:01:31 GMT  
		Size: 51.3 MB (51340699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d858f8b56955052faad08a5f4f04dd9a4348983879b7281d5a0c1e31915cf`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d18218e1bbed5bb7c7afa1ac19bd9d780c074848b504c6c610c3e8dd14d6fd`  
		Last Modified: Wed, 03 Dec 2025 00:01:46 GMT  
		Size: 169.1 MB (169119935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a972aa365b0a7dbfb6fa888c2411194ade10bcf53fcbb4331a96fd7c521d41`  
		Last Modified: Tue, 02 Dec 2025 21:31:54 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9800dc7871258ee59803cd7506d9ae5874e76c8b39e02fae9361a952683ecf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955dd22ff1a0973bcf2c1bd7c6d2bd4249fa04f96536fe7c8bf71f75db235904`

```dockerfile
```

-	Layers:
	-	`sha256:6cb2348819f85d1fc45f0f8691b27621e7f6b12b875f0309ce370d7e65c4af87`  
		Last Modified: Wed, 03 Dec 2025 01:03:10 GMT  
		Size: 17.8 MB (17815016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12c35ca577969357a00e18114cc62424ad2a6838643723693ed222ac15e471f`  
		Last Modified: Wed, 03 Dec 2025 01:03:11 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:de9b7ed3645e812625c5201d1a68ba099b527beda9d787ad434f0aba380c4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269797678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70452886a6843d6139d6d94a74f9c3521b5605de1eb7374ce495dab3c30c1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:29:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 21:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 21:29:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 21:30:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 21:30:03 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:30:03 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 21:30:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 21:31:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 21:31:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 21:31:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 21:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 21:31:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 21:31:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c300468ab11e2cdf09c00ac798ef40faf82a371def2fb015eb96cb32e251e8f`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9d4fa67c322cdf0414f9bdf1a49e0c3ad7f8046ef64658be051f824e2d489`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8087b6eefb6a411e20156e250185d9181a82e733c01a9a175c73bc3a8417c983`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.8 MB (5800484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c73678857f65572d049bb6cd9c8e9c73e1faee8a0c865e2b9e7d9fc318d8be`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267b660b2a4c4dca46206456f47928919ae976cf7096ad11e9b9354d4efc020`  
		Last Modified: Tue, 02 Dec 2025 21:32:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1a9fdd6260d6fe8886c0e03149856678298c675b56e27f45741be27b1f224`  
		Last Modified: Tue, 02 Dec 2025 21:32:22 GMT  
		Size: 50.0 MB (49960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127182a7d094325a8aae07825fc2fd0664952d22ce79a0de0516ae4037b60945`  
		Last Modified: Tue, 02 Dec 2025 21:32:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804f5e6ee90428cce4316b8c5bd6f510acbb851f0734c21c530d9cd75cc384`  
		Last Modified: Tue, 02 Dec 2025 23:13:42 GMT  
		Size: 167.4 MB (167392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a405e5ad57c91af79f4710a0639671b56cda9d51e2eed0e35b6f66e43db6686`  
		Last Modified: Tue, 02 Dec 2025 21:32:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d2dc7ed319b4cfa53587e1975d5534195aab8b41df71f60df0442be6e964256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb57f0c5b5c8241fd1a566f9dcd1470e923c85f17f4b232080cb514406d3dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e1af6b70b451f2006b311e8233cf89e0ef13b63b99d39533d2b815000db291b`  
		Last Modified: Wed, 03 Dec 2025 01:03:25 GMT  
		Size: 17.8 MB (17810159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46e91f1d4eb48dd03e29b5968329557348dd8cca1ca851f95440a0a865cfa12`  
		Last Modified: Wed, 03 Dec 2025 01:03:26 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
