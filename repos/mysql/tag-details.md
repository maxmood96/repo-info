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
-	[`mysql:8.0.45`](#mysql8045)
-	[`mysql:8.0.45-bookworm`](#mysql8045-bookworm)
-	[`mysql:8.0.45-debian`](#mysql8045-debian)
-	[`mysql:8.0.45-oracle`](#mysql8045-oracle)
-	[`mysql:8.0.45-oraclelinux9`](#mysql8045-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.8`](#mysql848)
-	[`mysql:8.4.8-oracle`](#mysql848-oracle)
-	[`mysql:8.4.8-oraclelinux9`](#mysql848-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.6`](#mysql96)
-	[`mysql:9.6-oracle`](#mysql96-oracle)
-	[`mysql:9.6-oraclelinux9`](#mysql96-oraclelinux9)
-	[`mysql:9.6.0`](#mysql960)
-	[`mysql:9.6.0-oracle`](#mysql960-oracle)
-	[`mysql:9.6.0-oraclelinux9`](#mysql960-oraclelinux9)
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
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:529b4afa138686871cf698617ef6e347a857179fa2c58e6811b6c20862a1cd6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b28c8bb8c1b9d9f9b3dbef6295e1c7e3d16cdfef879e9a7ea3099daa312e708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232276823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4e627a5e7e0a8ee6d5e8e6654781abe48540d2a68a69f9b5edb4017f6ed10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641ac6bb99741d68266a3a538a81e489a769c5c53a847dc0f275c06ffd74117`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cfd83619ebedaf236d9e7a7feb67086e8a280d60adb221df5b927ebf1de13`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 49.9 MB (49909484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b9c9ef01e4ef4eb3e3d0a92221d571639b9ba093f9b644ac1a668e09f4ac22`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc1d5ebae483a60fc0f19e6ddaa718cf08e621615b14f079f3ae72a42094a4`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 128.1 MB (128093739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ea9601bec89300e6a3ea54fdc867e2c1ec817aa3492b3aa4b7ece637db63a`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ad78a0e00495bd6f4a5229a58b8478acbd9c02ab70ab39a2ede5670b81527`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e464c6c22f4432692413f7f8106e1855640b1c9b38338f804a914bc04288d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6810ee9ba6abe37c06250e8f0ddd4c175e9bf0868ff0ba8f57be3334e43721c`

```dockerfile
```

-	Layers:
	-	`sha256:96fdc86d137636ddef5b7884d626abd57b163e36cddf02866408cbdff3e84cae`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f86fb85099ab9eab9996fba8c81c79ec46b4349ca2fe13a1c1fbcfedb04d15`  
		Last Modified: Tue, 14 Apr 2026 19:17:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19cfb5a4ddd4ec1b7efaeb902d829043a416f5dad3317c0912147e1853f97329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227880967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b37e2679315670d3fd53192602c40df839481c66fc1bceb107a416cbc5a31a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:15:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:16:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 19:16:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 14 Apr 2026 19:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:16:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:16:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a79c8668637e939b206794fe666ccbd91b17370d6761d137c4d84d8d8d2bc4`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ca300ffcd7d854ef9c2a06cd8046621a231875a6790c3b7619b5f2ca1263`  
		Last Modified: Tue, 14 Apr 2026 19:17:11 GMT  
		Size: 48.8 MB (48769340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57625cf440a6a7faa26efacf66d1047fd0de3fc24bc4367fce83ffb2b80f3d5d`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44694e56b891ec0a150c126cf44b0641f74e9c96d8a95c208c82593b30e37f89`  
		Last Modified: Tue, 14 Apr 2026 19:17:12 GMT  
		Size: 126.7 MB (126672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96495ec72e9fabc219aedc5e94a2fb2dcf32ca8d78c776a88b6dc051a6d686`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772b69f4298c22ae280a91f5e83eba0521fd0ea69d03f2d6d0c7259aba89e8`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:678d325e881629fa3526815c51c809ad38b4c01f19886b7b1b8be481df915554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6f873741a9f957a026a42cce5d7a9dad83a54c2b6caeea7a53d1fab9fcd4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3711edbe1f5bb1e13aabebeab8826409a3beac588d93434643920f0218632181`  
		Last Modified: Tue, 14 Apr 2026 19:17:09 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216a0cbaf7e0261a54c26b48f88b0ac12d381bc283a29ce7eed5e9b84d81fab`  
		Last Modified: Tue, 14 Apr 2026 19:17:08 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:669b2d89f3916f5263af230ffa20889a03c7f4bedf58133fe8780466c613f7ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:099e9934d866df75fa8c21eeb6e15989a93dda87949fa93f9ef9398efd0e6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9b45bc6f8372710ac9adf12b2ca61acdbd65f016acda9030f7772d5de3df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7ca25c5d7016eb042d320fc83e214090871f37f3ff54b57785ed68d8508`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f1113d05c84437facce2b1ec6fd109cd02e08e578f493d9cd0ecfda9b29e1`  
		Last Modified: Tue, 14 Apr 2026 19:15:22 GMT  
		Size: 47.8 MB (47801243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab658e78ae35cb38ec8fd0e85620143cf07f9b10124c3c3c46daa94997d01a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bbd266f165eec90fd5c851888f6ec4c9a3cba10114f45b872bd1f3326d74e`  
		Last Modified: Tue, 14 Apr 2026 19:15:24 GMT  
		Size: 131.1 MB (131130439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690f83bc4e2b1f4aaa5c1bc555d22fb9b173a8737986f6c6f369a12cccb9acd`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:acbdbc9380eda6b4a45f44ba2449b4cd84d76fb1c97841010c6d9b9c935dff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcef0acbdb24d65352c4b2c1ae39c30836b7da03b88f4589be7c3243df1dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8b72082969761d23f1cf651c405073be8647e04e701572c5dd8eb1b9824e975c`  
		Last Modified: Tue, 14 Apr 2026 19:15:21 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107caf581e827391d4d7270870eee9fd25a9265504a140f22fbc84ecf2454dd`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e3e388934566bdb453e0e63194bf27b484cebbdb3f79514376590f4fa2f764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c434a02d5ed7fcf8523b0638b3ff568fcfcc4e4ebdcf5b2a3546a66b065e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:13:42 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:14:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Tue, 14 Apr 2026 19:14:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:14:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:14:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:14:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29bf9ffbc53c8ec7070f803cac7f8bd5d8b4e054610eb7896196f34f85c47b`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3eceb21d57a42750aa768da39d353931115b8d4a894a71228300026b4a494a`  
		Last Modified: Tue, 14 Apr 2026 19:15:20 GMT  
		Size: 46.7 MB (46693266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192a86a77952bfa51ec36019b1f025acf7ad9e23393accfaa21ef2903fe92f7`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957f51e73eb8764ea9ab1baa0a07c6a488ee7bcb3930ede884514768cbfc073`  
		Last Modified: Tue, 14 Apr 2026 19:15:27 GMT  
		Size: 129.5 MB (129541713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee63a712f0af9c6d7a08d77de92e9a9a370565a43345bad479be0ae50be45e2`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ceeca23847f98046e194517648707821849ea9684087bea2225dda8495b0837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9ad2477976df93843a3190d3cf6f125a068ee1238cc871d00273f3282b60c`

```dockerfile
```

-	Layers:
	-	`sha256:005254225ce7a10792f17fb913845f0c40a002d41dba8df0843fbdc867817195`  
		Last Modified: Tue, 14 Apr 2026 19:15:19 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a660a1e9d7e29419b2e4abe79ddd8c74d496fbfc32297ca028a3653164062c`  
		Last Modified: Tue, 14 Apr 2026 19:15:18 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
