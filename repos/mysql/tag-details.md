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
-	[`mysql:8.0.41`](#mysql8041)
-	[`mysql:8.0.41-bookworm`](#mysql8041-bookworm)
-	[`mysql:8.0.41-debian`](#mysql8041-debian)
-	[`mysql:8.0.41-oracle`](#mysql8041-oracle)
-	[`mysql:8.0.41-oraclelinux9`](#mysql8041-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.4`](#mysql844)
-	[`mysql:8.4.4-oracle`](#mysql844-oracle)
-	[`mysql:8.4.4-oraclelinux9`](#mysql844-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.2`](#mysql92)
-	[`mysql:9.2-oracle`](#mysql92-oracle)
-	[`mysql:9.2-oraclelinux9`](#mysql92-oraclelinux9)
-	[`mysql:9.2.0`](#mysql920)
-	[`mysql:9.2.0-oracle`](#mysql920-oracle)
-	[`mysql:9.2.0-oraclelinux9`](#mysql920-oraclelinux9)
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
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 07:02:46 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 07:02:48 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 07:02:55 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 07:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 07:19:51 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 07:02:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 07:02:40 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 07:16:51 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 07:02:49 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 07:30:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 07:02:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 16:02:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Wed, 05 Feb 2025 04:01:29 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 07:02:46 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 07:02:48 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 07:02:55 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 07:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 07:19:51 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 07:02:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 07:02:40 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 07:16:51 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 07:02:49 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 07:30:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 07:02:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 16:02:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Wed, 05 Feb 2025 04:01:29 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-bookworm`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 07:02:46 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 07:02:48 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 07:02:55 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 07:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 07:19:51 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 07:02:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 07:02:40 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 07:16:51 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 07:02:49 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 07:30:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 07:02:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 16:02:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Wed, 05 Feb 2025 04:01:29 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-debian`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 07:02:46 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 07:02:48 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 07:02:55 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 07:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 07:19:51 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 07:02:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 07:02:40 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 07:16:51 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 07:02:49 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 07:30:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 07:02:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 16:02:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Wed, 05 Feb 2025 04:01:29 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oracle`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oraclelinux9`

```console
$ docker pull mysql@sha256:50b5ee0656a2caea76506fe702b1baddabe204cf3ab34c03752d2d7cd8ad83fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:782d31035f4936a200fdb42653ab2c77b074fc483feb23b9dd3b2804fc5c685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616596982edbd1559c47c8250b382ae55742a53d1edc132f2e183421ee573c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d8d3809b3122b261ce1e78f61a3bfd00a96be96bc6fa9a2ad57032b84154d`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157a7408a55d2d848c1d6d20eeb42b2a36d0421d3d49abe8486ea3cd09dca98f`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405af89949fd9ea55c97363dd5fa767c702ab38b0cf7e089ffb8ab91a4374fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 6.9 MB (6896392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92147eb338287e2a360f971d0d7ac5a5176f36fd00d4cc75a3b1d6b1b68e790`  
		Last Modified: Sat, 15 Feb 2025 04:02:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec9882b9768d297c2a190154ec8513c4e7775774d3f0681e1b0623d049d3a5`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad072341f26b862e6409b0848afeac2a677d69d09ee2cbfa62941f7b7bc9b873`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 49.6 MB (49623299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c2eca56fe01d2efa59b21e5a98188f39f70b70d69a35d89c7179bd821f6a`  
		Last Modified: Sat, 15 Feb 2025 04:02:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5c46ac97d217e0ca7637c9d5abcd39a8ddcf59db784e84cba630afe98a246`  
		Last Modified: Sat, 15 Feb 2025 04:02:26 GMT  
		Size: 125.3 MB (125293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd34fa224e6f2a03075b506b697fa9235eb28ec12f1d96f68cb1cfccc69fa32`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4144aa75defbd97123bb0c72b2cc8a39f426f89a1cac2e06b44651b6e8d19d4`  
		Last Modified: Sat, 15 Feb 2025 04:02:23 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a39f2fbe044112955cb724f3f5f91117006cfcb64ce897413b09c0a086c7ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194d4f6bb16a632600cbc109611b1436c92cd08ea7dae9ca911f298f6a42df`

```dockerfile
```

-	Layers:
	-	`sha256:ab84dfc44e396259c7f39359529a06242052ccba41e2208d4bda1f4a19b024e2`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 13.8 MB (13797395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56a2e313ecda19482cbb89f69c64d3771f3c4485b997695f763346e3a5fe5fd`  
		Last Modified: Sat, 15 Feb 2025 04:02:24 GMT  
		Size: 35.0 KB (34952 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60e2c5ec897acdc4b188ecbec2c2c11f2f511e0afd1c91ccf8d7f5d3d6e52e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea077402e99fa58f07d4cb3b5f166e256baab18cb68059734db2356ce8fcbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6cde00d59d96ff3f779c99274d160d5d21a9dbd8f2c1e7860b6c544d0574`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a5e0bee8064f842aaea899f26e0762ef02056bda47413d3ba2e2749847a4b9`  
		Last Modified: Sat, 15 Feb 2025 12:51:11 GMT  
		Size: 48.5 MB (48506309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882305ba978d8f93d7b594a1de0ce6b3e510df8dd2f628dc5eaa5c43fed8e0f`  
		Last Modified: Sat, 15 Feb 2025 12:51:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7678a5083faf1bd1698cd7e2f1461dc28cb010910721ed2b7d018f50553ef25a`  
		Last Modified: Sat, 15 Feb 2025 12:51:15 GMT  
		Size: 123.9 MB (123936301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ddadd108458180edacd25a6c35f45b572dc89c273a56ad6dacdf69f6f451b`  
		Last Modified: Sat, 15 Feb 2025 12:51:09 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd907af04ceee6e034ffbac79ae2a1c92f0070e7d909d9cd9a559c709d070ff6`  
		Last Modified: Sat, 15 Feb 2025 12:51:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:c607fdb2c06cde8caaf00f243f8272719538286eff011fd82c4a1dd8f4a4be09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e38903bee99a71ac441a1f3f28d7beeb531c0356181e01e818dfdb62f7db73`

```dockerfile
```

-	Layers:
	-	`sha256:8cd568e8772d33f2c6c19d4720e1db451fdb7e7b4bf85c7fc62e34668ec2b801`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 13.8 MB (13795743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5f81466148d44e70f7633a697090da3b578b96af529b01f6aeb85626cc627`  
		Last Modified: Sat, 15 Feb 2025 13:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oracle`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oraclelinux9`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oracle`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oraclelinux9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oracle`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oraclelinux9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:0917ecc5863323a48203dda0bb7d58582d958da62914024c474bf2e8c5f5ee73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4db12d62c1220d4f9b77b51005affcc7d981d97414e14c5e52013034f9b609da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232894541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9755c387b39e71d6f2f8f04b57c9461bf14c8023cb8105768a6e79936f62ed02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4990895e9b74cf9071bf5cdb6d0d36d47ef94419e29d6c42baa75386533962`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8168080d59c12bbe7034d285389e9aff202379512575e29f892c6931a16ad6`  
		Last Modified: Sat, 15 Feb 2025 04:02:14 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a8777e75425e8d3aa258f65d7c2a8b8c82af059530ba8638492a944fbd5fc`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 6.9 MB (6896391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf8eab0d7260b39207320cb1201e5a646452c2b2c54c7710bb04198d047123`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d73b138d48db874aa47dc39a6555e8643850e961fdd5b1ec4a5c4bbc34758`  
		Last Modified: Sat, 15 Feb 2025 04:02:15 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966698f1fbdb7ecad4d6a0fa4ca0ad76a20971d6027deec36030e21ab2da62b`  
		Last Modified: Sat, 15 Feb 2025 04:02:17 GMT  
		Size: 47.6 MB (47587882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227358103edfe3727c637c274b331982d2a15a1ed158e424ad6b2c42003222de`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155d1f8af49d29cdb97498f5700d0793aeb79b68262b661e8558056d80daf2c`  
		Last Modified: Sat, 15 Feb 2025 04:02:20 GMT  
		Size: 128.3 MB (128326902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bda43a95fb3485ade3ebb57beb4895971f0b0a6f8280c55b82cb578655bef6`  
		Last Modified: Sat, 15 Feb 2025 04:02:16 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15155299b2db9be0e93b5bad7c76ece0dcfea897d16ba2892cc13985a787bd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa68c70582dfa66badf0ac1e424864313c78fe20b0b9b0311d6f706da46a4e11`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ae0bcbf4c9db650bbe37980963eefc6782ef929e4f297a61400d308d9f478`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 14.1 MB (14074216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd52b91195cc1f12a7672d5b233c914b91ef619188c4bdfca793145ae1bd463`  
		Last Modified: Sat, 15 Feb 2025 04:02:18 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85fbf0eb4650e0ea2e141095ef0fbcc2f226f238d66a7e1c3af2f5c6c414bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f6dc0eed0a1873e2a013bb76c282a48eb3a0d825430f165e3dedbb940d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355b97fa6b39f5a567bca04ae836cedaf30db69d094c81ff156cff402afc20a4`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3c76ec2bc10a9d6f7e97d77e07a14beca01793484a15db2635874851e108d`  
		Last Modified: Sat, 15 Feb 2025 12:18:13 GMT  
		Size: 46.5 MB (46468963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad65461c369576c8359fe87f689330a2d88b0b6ebf40442f433713a5e9109ee`  
		Last Modified: Sat, 15 Feb 2025 12:18:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8658491a3a8ab1001b110138328333fa54f0c8b8440c3a697f774f1025c598`  
		Last Modified: Sat, 15 Feb 2025 12:18:19 GMT  
		Size: 126.8 MB (126796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fd35c7a1a4ffe928b8eb8c90a62c264263971d9ef9feda2cf1871d3333227`  
		Last Modified: Sat, 15 Feb 2025 12:18:11 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac78a5cb4630e0bdeeeadf0e9b32e8bd49279735fce536d4374c8ba8fd123b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8580e9ec6028756aff8ba8412df82ddad435559f48f0ea4e827f63ef39ac22`

```dockerfile
```

-	Layers:
	-	`sha256:93ea343f78feba10180a0d5228e4ee91d27aac6205e1ccd6da0e0efd58179ee5`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 14.1 MB (14072636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c509e837de25158cfe9e2e2f93945299371a0ab73eef77d2741b9462c3e34186`  
		Last Modified: Sat, 15 Feb 2025 13:02:36 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:146682692a3aa409eae7b7dc6a30f637c6cb49b6ca901c2cd160becc81127d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c32cc542bb409c5da8a172c09e712e8b1f1e10eea9eae534f55a07fc5523021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241129028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5568fddd4f66008ebae555bfee3e999a8f8e6516fbe974e0af11013e83e241fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255dceb9ed5ca16ec8fd57a7e943b181a42df9b958e5bc3141832ef0a4f27a9`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d22e42ea507021b59c28a10a46bbd78aad0265fb0f48a7701e12fdf59deb78`  
		Last Modified: Sat, 15 Feb 2025 04:02:35 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b106548a3a3a23650afc7b8f9014850a6531bb558cba27dd83990e349159e`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 6.9 MB (6896382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0d473cadf57f6edab39bc3a72e756581bb07403ab62ca0b8bc596158456a6`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a22f949f96710b6cf02b368fb66fc017a064f020c2de8eddb50d28c59ae06`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab5f6ddde04c70c3f5e76470830d69244fc6eebcabcf94e1bb3a7a23e4ca1`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 48.4 MB (48419748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ba1ac457aae51c4790f91d75f35d858e51b6b1186761e7d38498229e73844`  
		Last Modified: Sat, 15 Feb 2025 04:02:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9646b08259deeeaa32bd8e49a57340dc7660f0390dc73e3b918dd1f83a26bb`  
		Last Modified: Sat, 15 Feb 2025 04:02:42 GMT  
		Size: 135.7 MB (135729521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b018337e2af9fa2230e06fdbd62cf02824f16d5dbee7f0ffc635b2dc4c140`  
		Last Modified: Sat, 15 Feb 2025 04:02:37 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d6419dbe8c5b1881ea7a537d4bbdc05a3d24af56330e1c22e78f428d7aebf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dd77564c6a1e298772d672665c6af67df5d064b9e9f9b6865f0c67257e493`

```dockerfile
```

-	Layers:
	-	`sha256:266d393929e5e11da1121fdc05e2b6c9adceee4a1c3dcedddab5378f2973d1aa`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7e3146b6eee731bc563435bd3aae955afdcf48bccc1a28e3bde608a83f63d7`  
		Last Modified: Sat, 15 Feb 2025 04:02:39 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45fbe1d12a60e067283110f55c0db4e81786d7c5571cdd08ef49317053125d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236506734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8e7cf9efaa18969a6e2ea5ce0ee01b5c0fa9689adb25ae120876299af0883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae24b624fed8d28caf26ef92042e91f38f167c4dbd19ac9f0ee5696010df2`  
		Last Modified: Sat, 15 Feb 2025 11:19:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1014e2965276e4a4c650ec3d85da80e296fca44cb37a346162587b561ce693d`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 913.5 KB (913453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6251984b19cd7b28ae6078b24e52b5b962c6a9a944eb68e9b69f95f674aab`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 6.5 MB (6492775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e176816781e58b2d87ef65abac7bedfadf7a9274cde2b01a6130cf60b4c42b41`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf46058f45cbbe81b9d80ccada47788c2c1f01d5ba232207f8d42178c6f8dd`  
		Last Modified: Sat, 15 Feb 2025 11:19:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d32318ef6d2e20e768d25820346481187ca3f1366aea26a9786bb00c5fdaf7`  
		Last Modified: Sat, 15 Feb 2025 11:19:35 GMT  
		Size: 47.3 MB (47296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcba864ffae72cc219d450a33749416d0fc52787a1a6eb4fa2c663f84fa2a623`  
		Last Modified: Sat, 15 Feb 2025 11:19:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d78c46a16ebadd30e50efe205d5d0b582f7d770f4d96e39c6427c171c8d67`  
		Last Modified: Sat, 15 Feb 2025 11:19:39 GMT  
		Size: 134.1 MB (134125622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5645ac95474c80022da94c144cd54daae321dc54795eeed55328b51459f9f924`  
		Last Modified: Sat, 15 Feb 2025 11:17:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:050bc4170768cb87e8e7c96037c49aca308e3cf11dfe00d5128f8ff5530c0e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9197598c7fef872f62de762da9c18d6e1e83f53143c35260985789b5bc4d70af`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ce887f562951926f2f1416bd00d74fda9ad56caca786804dbd8e775f288a6`  
		Last Modified: Sat, 15 Feb 2025 13:02:46 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45799f0fb4524da08e8b1bb4831c5e80566e19b3b05d7ba7e05119109886c404`  
		Last Modified: Sat, 15 Feb 2025 13:02:47 GMT  
		Size: 35.7 KB (35658 bytes)  
		MIME: application/vnd.in-toto+json
