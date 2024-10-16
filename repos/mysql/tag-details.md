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
-	[`mysql:8.0.40`](#mysql8040)
-	[`mysql:8.0.40-bookworm`](#mysql8040-bookworm)
-	[`mysql:8.0.40-debian`](#mysql8040-debian)
-	[`mysql:8.0.40-oracle`](#mysql8040-oracle)
-	[`mysql:8.0.40-oraclelinux9`](#mysql8040-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.3`](#mysql843)
-	[`mysql:8.4.3-oracle`](#mysql843-oracle)
-	[`mysql:8.4.3-oraclelinux9`](#mysql843-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.1`](#mysql91)
-	[`mysql:9.1-oracle`](#mysql91-oracle)
-	[`mysql:9.1-oraclelinux9`](#mysql91-oraclelinux9)
-	[`mysql:9.1.0`](#mysql910)
-	[`mysql:9.1.0-oracle`](#mysql910-oracle)
-	[`mysql:9.1.0-oraclelinux9`](#mysql910-oraclelinux9)
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
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:950fb1005655086a87e322d2c0a4c34c0e1a99d1b268029987b9b01dc6321eeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:6b143fc1f4eab6fc9d20f383cd108c680170ff22678c5cd28551d35247fed0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167076816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da8fc4b539c8ff9005b316b41b09d99b6ef6cdf55b5abbfcfd40dd3547f845`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c54a7f9fe815e299b650e2a42aad4f236740b6af3353893d8214f795bc70ac`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972686f20d79b40117d39ca73b5b034a013cc865e57f330367ba0157679691fb`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5f58971f7de31c996b9d164627887ad94bfb12897700798a4420d52eb0267`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 6.7 MB (6733386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3daf5de485432cea017d47fb499c82e5f61883b9beb5aad9eb8b42961fd0a9`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba13b8088fe1252f16f0722d9e2d3a04cd938138cd748e38e5f2d78234fc858`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514ee5d23bc92938bf617f59570e6436c2138daf8fce4171c3d32ffaeb12de42`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 49.2 MB (49176281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f47674d2509d1cf19c5b24b75579133d375fe358b7d1fb40a4fb783167b1f`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077dbde9e2f694950fbdc9cb268ae8a034d464c0373156a34eae02a32b4661f9`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 60.9 MB (60927625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466b47b075c45f6750c0457257324f02b71de861329b12935ecceb2dac1bc044`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145be117b98dbf2dabf0e7199ac541ba7493e346cb909e2ee225f92ce86c6dd`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d0cce168e23a738534735a512c6e33c7e0accc082da3683e6d86c3fb80470867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726275b48978f0a0ab651fe4fb236b76a65eb1fc0960373710388f72d7f697b4`

```dockerfile
```

-	Layers:
	-	`sha256:f5754cd3d63420a66dbc385619df2cf4b0efeaf1828593ae0954dfd02e250cc3`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde629056a3e58cf0a82df9d909b7721909c570d9bd9f8728cf84134819fb338`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:f5217f5fd0ecd0b1e2ae9d99ef9facee80a14562aa5f08b25e95a39496e0f242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:28703d027e29c319364627114866865ccb34c2b237e83b933bf73b9b65d91fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184747902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c716403fbe7617d7487cdc9060a8099ee7091d86212e9f0d7bc657a4fe27044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9340832f4f653bcecc2dd26a7064d360f5bfa8b10bd8d6c1599255bc1bc914b9`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599147bb41b49afe7e03c17661f874924741e230702351a8a3bf9565e706a80e`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 4.4 MB (4422727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1bde57bb6e16de0a1a9764880c9ed58cc04531e991705f22b44989b21c41c`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 1.4 MB (1445892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf26310255b838c9720be3f62f5e57cf9dde36ee8f4ae5cdf74d7a6e41b7fb`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6ec81abedddaae798ce6acaafdf212af666240be085ccec47359019aa9fffd`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 15.3 MB (15294815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73eb3f31f661326e5f29752965c66662a483577d00b7e13674016009cac16b5`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef2bdf8bad54564e01687776d9f03143cfd16a544bcab1c4586b37219ba644`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adc78b691f30093cae87a386d4467c885443653796e3ccd2203a3ca229a0a61`  
		Last Modified: Fri, 27 Sep 2024 06:16:48 GMT  
		Size: 134.4 MB (134447932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b939f15cca2ea04812b6bd0b453819949e70ef200f37176198dccdffea82`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb436fe59e13b3e5d885be38d5faf91c8df81ee4dc86a774a7f215f57cefd71`  
		Last Modified: Fri, 27 Sep 2024 06:16:47 GMT  
		Size: 5.3 KB (5321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0125f1e35a95bbcef99e634033615962a9454cdc70043d3b77a7c357016fd1b`  
		Last Modified: Fri, 27 Sep 2024 06:16:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:dcbee172f7b139c0ae080e71ed47dff0e523fc9cee975eaebda9965d15584fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e016400b03bce9f7c1221a0548555c418a2890b93b94846ab4801b3d6567d3`

```dockerfile
```

-	Layers:
	-	`sha256:b99ffa4ff2a65e0b84aa87c92617c2644fdd6b1edd70a52d1aaa2193c701c28b`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c876151697f9e52c843d24dff7b728804da75f54e06de0bc4485e832eb564a7`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:f5217f5fd0ecd0b1e2ae9d99ef9facee80a14562aa5f08b25e95a39496e0f242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:28703d027e29c319364627114866865ccb34c2b237e83b933bf73b9b65d91fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184747902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c716403fbe7617d7487cdc9060a8099ee7091d86212e9f0d7bc657a4fe27044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9340832f4f653bcecc2dd26a7064d360f5bfa8b10bd8d6c1599255bc1bc914b9`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599147bb41b49afe7e03c17661f874924741e230702351a8a3bf9565e706a80e`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 4.4 MB (4422727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1bde57bb6e16de0a1a9764880c9ed58cc04531e991705f22b44989b21c41c`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 1.4 MB (1445892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf26310255b838c9720be3f62f5e57cf9dde36ee8f4ae5cdf74d7a6e41b7fb`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6ec81abedddaae798ce6acaafdf212af666240be085ccec47359019aa9fffd`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 15.3 MB (15294815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73eb3f31f661326e5f29752965c66662a483577d00b7e13674016009cac16b5`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef2bdf8bad54564e01687776d9f03143cfd16a544bcab1c4586b37219ba644`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adc78b691f30093cae87a386d4467c885443653796e3ccd2203a3ca229a0a61`  
		Last Modified: Fri, 27 Sep 2024 06:16:48 GMT  
		Size: 134.4 MB (134447932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd13b939f15cca2ea04812b6bd0b453819949e70ef200f37176198dccdffea82`  
		Last Modified: Fri, 27 Sep 2024 06:16:46 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb436fe59e13b3e5d885be38d5faf91c8df81ee4dc86a774a7f215f57cefd71`  
		Last Modified: Fri, 27 Sep 2024 06:16:47 GMT  
		Size: 5.3 KB (5321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0125f1e35a95bbcef99e634033615962a9454cdc70043d3b77a7c357016fd1b`  
		Last Modified: Fri, 27 Sep 2024 06:16:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:dcbee172f7b139c0ae080e71ed47dff0e523fc9cee975eaebda9965d15584fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e016400b03bce9f7c1221a0548555c418a2890b93b94846ab4801b3d6567d3`

```dockerfile
```

-	Layers:
	-	`sha256:b99ffa4ff2a65e0b84aa87c92617c2644fdd6b1edd70a52d1aaa2193c701c28b`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c876151697f9e52c843d24dff7b728804da75f54e06de0bc4485e832eb564a7`  
		Last Modified: Fri, 27 Sep 2024 06:16:45 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:950fb1005655086a87e322d2c0a4c34c0e1a99d1b268029987b9b01dc6321eeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b143fc1f4eab6fc9d20f383cd108c680170ff22678c5cd28551d35247fed0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167076816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da8fc4b539c8ff9005b316b41b09d99b6ef6cdf55b5abbfcfd40dd3547f845`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c54a7f9fe815e299b650e2a42aad4f236740b6af3353893d8214f795bc70ac`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972686f20d79b40117d39ca73b5b034a013cc865e57f330367ba0157679691fb`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5f58971f7de31c996b9d164627887ad94bfb12897700798a4420d52eb0267`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 6.7 MB (6733386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3daf5de485432cea017d47fb499c82e5f61883b9beb5aad9eb8b42961fd0a9`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba13b8088fe1252f16f0722d9e2d3a04cd938138cd748e38e5f2d78234fc858`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514ee5d23bc92938bf617f59570e6436c2138daf8fce4171c3d32ffaeb12de42`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 49.2 MB (49176281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f47674d2509d1cf19c5b24b75579133d375fe358b7d1fb40a4fb783167b1f`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077dbde9e2f694950fbdc9cb268ae8a034d464c0373156a34eae02a32b4661f9`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 60.9 MB (60927625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466b47b075c45f6750c0457257324f02b71de861329b12935ecceb2dac1bc044`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145be117b98dbf2dabf0e7199ac541ba7493e346cb909e2ee225f92ce86c6dd`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d0cce168e23a738534735a512c6e33c7e0accc082da3683e6d86c3fb80470867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726275b48978f0a0ab651fe4fb236b76a65eb1fc0960373710388f72d7f697b4`

```dockerfile
```

-	Layers:
	-	`sha256:f5754cd3d63420a66dbc385619df2cf4b0efeaf1828593ae0954dfd02e250cc3`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde629056a3e58cf0a82df9d909b7721909c570d9bd9f8728cf84134819fb338`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:950fb1005655086a87e322d2c0a4c34c0e1a99d1b268029987b9b01dc6321eeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:6b143fc1f4eab6fc9d20f383cd108c680170ff22678c5cd28551d35247fed0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167076816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da8fc4b539c8ff9005b316b41b09d99b6ef6cdf55b5abbfcfd40dd3547f845`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c54a7f9fe815e299b650e2a42aad4f236740b6af3353893d8214f795bc70ac`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972686f20d79b40117d39ca73b5b034a013cc865e57f330367ba0157679691fb`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5f58971f7de31c996b9d164627887ad94bfb12897700798a4420d52eb0267`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 6.7 MB (6733386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3daf5de485432cea017d47fb499c82e5f61883b9beb5aad9eb8b42961fd0a9`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba13b8088fe1252f16f0722d9e2d3a04cd938138cd748e38e5f2d78234fc858`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514ee5d23bc92938bf617f59570e6436c2138daf8fce4171c3d32ffaeb12de42`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 49.2 MB (49176281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f47674d2509d1cf19c5b24b75579133d375fe358b7d1fb40a4fb783167b1f`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077dbde9e2f694950fbdc9cb268ae8a034d464c0373156a34eae02a32b4661f9`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 60.9 MB (60927625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466b47b075c45f6750c0457257324f02b71de861329b12935ecceb2dac1bc044`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145be117b98dbf2dabf0e7199ac541ba7493e346cb909e2ee225f92ce86c6dd`  
		Last Modified: Fri, 20 Sep 2024 18:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d0cce168e23a738534735a512c6e33c7e0accc082da3683e6d86c3fb80470867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726275b48978f0a0ab651fe4fb236b76a65eb1fc0960373710388f72d7f697b4`

```dockerfile
```

-	Layers:
	-	`sha256:f5754cd3d63420a66dbc385619df2cf4b0efeaf1828593ae0954dfd02e250cc3`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde629056a3e58cf0a82df9d909b7721909c570d9bd9f8728cf84134819fb338`  
		Last Modified: Fri, 20 Sep 2024 18:50:12 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40`

```console
$ docker pull mysql@sha256:b64e9c7fe7e377f9a30797f0073e2baaad96a1dc905fc4133573feb7b71b6e33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-bookworm`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.40-debian`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.40-oracle`

```console
$ docker pull mysql@sha256:b64e9c7fe7e377f9a30797f0073e2baaad96a1dc905fc4133573feb7b71b6e33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oraclelinux9`

```console
$ docker pull mysql@sha256:b64e9c7fe7e377f9a30797f0073e2baaad96a1dc905fc4133573feb7b71b6e33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3`

```console
$ docker pull mysql@sha256:8c61dfb4c3cb7899ba6e84eea3d9cbf2c01f7dd249609fd3aee5465ac5c4018f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oracle`

```console
$ docker pull mysql@sha256:8c61dfb4c3cb7899ba6e84eea3d9cbf2c01f7dd249609fd3aee5465ac5c4018f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oraclelinux9`

```console
$ docker pull mysql@sha256:8c61dfb4c3cb7899ba6e84eea3d9cbf2c01f7dd249609fd3aee5465ac5c4018f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oracle`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oraclelinux9`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oracle`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oraclelinux9`

```console
$ docker pull mysql@sha256:7c4b83b4f97f9426feb6b2812cf5e8ba23e6daf0a08b9339f98026a19570679c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:69bb51eed27e670a1750875cd07de79593ee1b125e21e27381c6c86735152227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0cf8b60f74e235c4dd4beb762b10ec6da3dce30265f5f1d40c2c11fa7872ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c757d623b1901eeba266f635e7e99cac9ae52bf30ab2056efa09219038dfcc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa3ee22beaac9bb5ecd20d13a796b7c7657df7f26f6662abdeabdebc917d05`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b24615ae8486427c10017b6ad269b05818039c2a9fd0e0ff25db3112a66eb`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 6.7 MB (6733422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded0449fb1aa6683e69ef2b99ef7620652d8d12bb1601f871d18a1ec472b82a`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095378692b4ad788a8f6b59c3ebecd283743b40ec5364014877041e87b1d32dc`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d87e5d2a3ba02265636e4f0d410acafb6cc78cd4dd9a64ee5df680ebb928c`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 47.7 MB (47706833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dbbbda514c7960b3c01eab00e03d0872aabc10aa6b52b99d9329af6bc1e26`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982f92841ea30038cbb9f564f3e4e2d07600fd52f01bc7509bbd8f891884efa1`  
		Last Modified: Fri, 20 Sep 2024 18:50:11 GMT  
		Size: 65.9 MB (65890994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34c1fda3aa4fbb704aaf26676a90a48cb1df95351a11e05ceca236b4d336e6`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8f19540c39e9e669162c1840aaad2eb676dcb75ac102f43e85a563abc56c7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d17cc8d90c1a39c35bd84f25ce9fa8932188632ba2a623b183236a22b18c30a`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3d67be574eb08b8c63c99255954983ec95079eae28a3081d9ea2f83978a0f`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa95ac42b234f0677660ed1e93f8934500b602785f1f193a534a60df0640fa0`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 35.3 KB (35281 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json
