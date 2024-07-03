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
-	[`mysql:8.0.38`](#mysql8038)
-	[`mysql:8.0.38-bookworm`](#mysql8038-bookworm)
-	[`mysql:8.0.38-debian`](#mysql8038-debian)
-	[`mysql:8.0.38-oracle`](#mysql8038-oracle)
-	[`mysql:8.0.38-oraclelinux9`](#mysql8038-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.1`](#mysql841)
-	[`mysql:8.4.1-oracle`](#mysql841-oracle)
-	[`mysql:8.4.1-oraclelinux9`](#mysql841-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.0`](#mysql90)
-	[`mysql:9.0-oracle`](#mysql90-oracle)
-	[`mysql:9.0-oraclelinux9`](#mysql90-oraclelinux9)
-	[`mysql:9.0.0`](#mysql900)
-	[`mysql:9.0.0-oracle`](#mysql900-oracle)
-	[`mysql:9.0.0-oraclelinux9`](#mysql900-oraclelinux9)
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
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.38` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.38` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-bookworm`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-debian`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-oracle`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.38-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-oraclelinux9`

```console
$ docker pull mysql@sha256:134e2d1c7c517d05e5328a77aa5a165a314dc4c4116503e7e089494f4e398ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.38-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.38-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c5065b48e6609ae57703442f011db91a2669d7e8d770e393f5d243d70b5ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171318131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb72f0e1879a1caf233241c36d3f5b3fec91a4582e864737e1bb7617d481e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c376092c399d492e28ecb18766524bc2278802a828c69e2869b98f2a5cf69f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ed501313128e173e5f4d84d0b7618a0e0bbe809443a1b27dfe6d213f3f19`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 48.0 MB (48031365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85e12a30ff8b1a9b752acd0af8355d6a3ef556c11cd01c79f5bc680607832f`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30523a79a31fc5a97d7cd1a945425f3e2ea70cd92e9c3f1b61cb26f8e6f972`  
		Last Modified: Wed, 03 Jul 2024 01:55:20 GMT  
		Size: 68.4 MB (68396106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9e9df8c1ce627a5da3097c39f87a99f2c242f44fc3ead76c845afd8694921`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2354cf53206ba25a285564176d05322030c269667afd34274e0eba380eed0`  
		Last Modified: Wed, 03 Jul 2024 01:55:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a594f9ced8409ef307eb9285394a232e483173557a3c6c6410ba73706e811579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2988f683c9865bc531a9b4c4b22ac34651f1c0809e098b1f86591d850c873c9`

```dockerfile
```

-	Layers:
	-	`sha256:03249d0fe670a298617342e13db9bbb5ad3b5532fd014acbfe42fb49a4fefbf4`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd949433951d4bc98c06bd05a8f0aa3f6db4ce5026ef2ebf2643f745061bf544`  
		Last Modified: Wed, 03 Jul 2024 01:55:18 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.1` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1-oracle`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1-oraclelinux9`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oraclelinux9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.0` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0-oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0-oraclelinux9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:d26a69e1ef146c77ecfddf3128134e3a0f4c6123133725835818107037649827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cd90cd2a970690c7f1f6fa48424dd57dd0f24489594ab345f15e30a957c186c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae74bfe975e8b3b2ee0efabd3bcc449e44e17e660c2f2b2b16da7c34231db42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f79194aff73d0b9d71895b0d1359eaa42a1daa6eef817aa5739ced01cabb9`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fa268231149c65a8a7de0bc1a7879f4450dd25fbccd4e22332ff11405a3ee`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 46.1 MB (46116084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760205fa121096b1d894fcbab1d94500b50d3885e7cbefe778b6eda22285a2fc`  
		Last Modified: Wed, 03 Jul 2024 01:54:03 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65c54694f501b1e98ed8d88160a0271766f473112533665d3790a17b8107ca`  
		Last Modified: Wed, 03 Jul 2024 01:54:05 GMT  
		Size: 65.7 MB (65730106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb26c7eb0577c7badb33c2afd01850a7065a11b2fea080e2d00cfe2f19a4f3`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f9f207d8202d27b93f9871ca7a514f39dd9d24cdf7bc52c0c1dfbfc03221ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a6d181f8ab67344cd7d17371926607f14205689e98ef52187e4713df481e`

```dockerfile
```

-	Layers:
	-	`sha256:8dc4ab7fe8a5e604701c9f6b3330a99062f36fae027271e82079f4c706ca43bb`  
		Last Modified: Wed, 03 Jul 2024 01:54:04 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de13bc40f42b59b70dec799f40f267426032125c6df977e8f4936d75dc144cd`  
		Last Modified: Wed, 03 Jul 2024 01:54:02 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
